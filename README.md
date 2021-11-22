# Control-M Python Client

Control-M Python Client is a python library to programmatically design, schedule, run, and monitor your Control-M workflows. The design of the Control-M Python Client is oriented towards data scientists who prefer a more programmatic approach and does not require advanced knowledge in Control-M.

## Getting Started

The best way to get familiar is to check the [notebooks examples](https://github.com/controlm/ctm-python-client/tree/main/examples/python_notebooks). Start with [Hello world](https://github.com/controlm/ctm-python-client/blob/main/examples/python_notebooks/Demo%2001%20-%20HelloWorld.ipynb) to get familiar with the syntax.

You do not need to have an in-depth knowledge of Control-M, but some familiarity with Control-M will help you understand the different job types and syntax offered by Control-M Python Client.

### Control-M Environment

Control-M Python Client requires an operating Control-M. **We recommend first trying it out in a sandbox environment!** To be able to run a workflow, you will also need an available agent. 

In addition, ensure that you have the required authorizations to use Control-M Automation API. These authorizations are based on API keys (for Helix Control-M) or users. Check with your system administrator if you have a user or api key that can use Control-M Automation API.

Note: Control-M Python Client does **not** require use of the Automation API ctm cli.

### IDE

Use any IDE you want, but Control-M Python Client is more fun to test with notebooks, so make sure that your IDE supports it. If you use VSCode, we recommend that you download/activate the Python Extension.

### Authentication

Control-M Python Client uses Control-M Automation API and requires the same authentication used in a Control-M environment. We advise you to get familiar with it, whether using [Helix Control-M](https://documents.bmc.com/supportu/controlm-saas/en-US/Documentation/Users_and_Roles.htm) or the [Control-M on premises](https://docs.bmc.com/docs/display/workloadautomation/Control-M+Workload+Automation+Documentation).

Note that Automation API allows you to programmatically create and delete authorization roles. Work with your system administrator to decide on the best way to provide authorizations for developers while satisfying your security needs.

For a quick way to create an api key with a specified lifetime, check our **create_key** tool in the **tools** folder.

## Installation

We recommend that you set up a virtual environment before installing:

```
python -m venv venv
source venv/bin/activate
```
In Windows:
```
python -m venv venv
venv\Scripts\activate
```

### Installing via pip

```
pip install git+https://github.com/controlm/ctm-python-client.git
```

### Installing from source

```
git clone https://github.com/controlm/ctm-python-client.git
pip install ctm-python-client
```

Note: You can use the library without installing, be sure to add the src folder in the python path:
```python
import sys
sys.path.insert(0,"<path-to-repo>/src")
```

## Creating a flow with Control-M Python Client

Examples can be found in the example section in the format of python notebooks or as python scripts. We recommend to start with the notebooks.

### Starting a flow
To start a flow you need to import `CmJobFlow`:
``` python
from ctm_python_client.core.bmc_control_m import CmJobFlow
```
Create a flow:
```python
t1_flow = CmJobFlow(
    application="Demo", sub_application="HelloWorld", session=session, ctm_uri=ctm_uri
)
```

`ctm_uri` is your Automation API endpoint

`session` is a session object.

To create a session import `Session`:
```python
from ctm_python_client.session.session import Session
```

and create a session either for Helix Control-M:
```python
session = Session(endpoint=ctm_uri, api_key="An API KEY provided by my system administrator")
```

or for Control-M:
```python
session = Session(endpoint=ctm_uri, username="myuser", password="my password")
```

Note: This is the only place you will need to distinguish between Helix Control-M and the traditional Control-M.

**IMPORTANT: Passwords and API Keys are sensitive information! Please handle as such. Never commit code with these!**

### Defining where and when to run

You created a flow! Now you need to define where it will run. Define the host (agent) where the flow will run and the user under which it will run.

Note: username is not necessarily your username. Rather, it is the user under which the agent is installed.

```python
t1_flow.set_run_as(username="user", host="myagent")
```

To define when to run, you need to specify the schedule

```python
# Define the schedule
months = ["JAN", "OCT", "DEC"]
monthDays = ["ALL"]
weekDays = ["MON", "TUE", "WED", "THU", "FRI"]
fromTime = "0300"
toTime = "2100"
t1_flow.set_schedule(months, monthDays, weekDays, fromTime, toTime)
```

### Creating folders and tasks

Your flow has a name and definitions for when and where to run. But it is still empty!
Let's add a folder:

```python
f1 = t1_flow.create_folder(name="HelloWorld")
```

To create a task, you will need to import the corresponding job type. Check what are the [supported types](https://github.com/controlm/ctm-python-client/blob/main/SupportedJobs.txt)

Let's create some dummy jobs to test the flow.
First we import:
```python
from ctm_python_client.jobs.dummy import DummyJob
```
Then we create the tasks:
```python
start = t1_flow.add_job(f1, DummyJob(f1, "Start-Flow"))
end = t1_flow.add_job(f1, DummyJob(f1, "End-Flow"))
hello_world = t1_flow.add_job(f1, DummyJob(f1, "Hello-World"))
```

Now, the last thing to do to complete the flow is to set the flow by chaining tasks:

```python
# start >>  hello_world >> end
t1_flow.chain_jobs(f1, [start, hello_world, end])
```

### Check your workflow

You can view your flow in a nice diagram by importing `DisplayDAG`.

```python
from ctm_python_client.utils.displayDAG import DisplayDAG

DisplayDAG(t1_flow).display_graphviz()
```

If you are familiar with using Automation API, you can also export your workflow to Json!
```python
t1_flow.display_json()
```

### Submit the flow

Now your flow is complete! You can choose to run it or deploy it.

Deploying a flow means saving it in the database. The definitions will be stored in the Control-M Server and it will eventually run according to its schedule.

Running a job orders it immediately, regardless of the schedule. It also performs a deploy, so it will continue running according to its schedule after the initial run.

To deploy a flow:
```python
t1_flow.deploy()
```

And to run:
```python
t1_flow.run()
```
### Next Steps

Once you have successfully completed the Hello World Program, try out the other examples! The examples cover more advanced flows with multiple job types and also with Application Integrator Job types.
## Contributing

Control-M Python Client welcomes contribution, to do so, please open a pull request.
To set up a development environment, use the requirements_dev.txt :

```
$ git clone https://github.com/controlm/ctm-python-client.git
$ cd ctm_python_client
$ python -m venv venv
$ source venv/bin/activate
$ pip install -r requirements_dev.txt
```

Please note that the folders `ctm_api_client` and `ctm_saas_client` only contains generated code. Check `ctm_python_client` for the interesting stuff ;)

## Links

- [Control-M Documentation](https://docs.bmc.com/docs/display/workloadautomation/Control-M+Workload+Automation+Documentation)
- [Helix Control-M Documentation](https://documents.bmc.com/supportu/controlm-saas/en-US/Documentation/home.htm)
- [Automation API Documentation](https://docs.bmc.com/docs/display/public/workloadautomation/Control-M+Automation+API+-+Getting+Started+Guide)
- [Automation API with Helix Control-M Documentation](https://docs.bmc.com/docs/display/ctmSaaSAPI/Control-M+SaaS+Automation+API+Home)

## License

See [License](https://github.com/controlm/ctm-python-client/blob/main/LICENSE)
