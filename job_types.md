#  CommandJob


#### Import instructions
	 from ctm_python_client.jobs.command import CommandJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  command   
	-  pre_command=None   
	-  post_command=None   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  FileTransferJob


#### Import instructions
	 from ctm_python_client.jobs.file_transfer import FileTransferJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile_src   
	-  connection_profile_dest   
	-  number_of_retries   
	-  s3_bucket_name   
	-  file_transfers   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  SLAManagementJob


#### Import instructions
	 from ctm_python_client.jobs.sla_management import SLAManagementJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  service_name   
	-  service_priority   
	-  created_by   
	-  job_runs_deviations_tolerance   
	-  complete_in   
	-  events_to_wait_for   
	-  events_to_delete   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  InformaticaJob


#### Import instructions
	 from ctm_python_client.jobs.informatica import InformaticaJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  repository_folder   
	-  workflow   
	-  workflow_execution_mode   
	-  workflow_restart_mode   
	-  enable_output   
	-  enable_error_details   
	-  priority   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  PeopleSoftJob


#### Import instructions
	 from ctm_python_client.jobs.peoplesoft import PeopleSoftJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  user   
	-  control_id   
	-  server_name   
	-  process_type   
	-  process_name   
	-  append_to_output   
	-  bind_variables   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  EmbeddedScriptJob


#### Import instructions
	 from ctm_python_client.jobs.embedded_script import EmbeddedScriptJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  script   
	-  file_name   
	-  pre_command=None   
	-  post_command=None   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  ScriptJob


#### Import instructions
	 from ctm_python_client.jobs.script import ScriptJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  file_name   
	-  file_path   
	-  pre_command   
	-  post_command   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  DummyJob


#### Import instructions
	 from ctm_python_client.jobs.dummy import DummyJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder
	-  job_name
	-  description=None
	-  host=None
	-  run_as=None   
 
 
 
 
<br/>
<br/>

#  AiGenericJob


#### Import instructions
	 from ctm_python_client.jobs.ai_jobs.ai_generic import AiGenericJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  ai_name   
	-  host=None   
	-  run_as=None   
	-  description=None   
	-  **kwarg   
 
 
 
<br/>
<br/>

#  AIBlobStorageJob


#### Import instructions
	 from ctm_python_client.jobs.ai_jobs.ai_blob_storage import AIBlobStorageJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  ai_action   
	-  ai_blob_name   
	-  ai_container   
	-  ai_file_path   
	-  ai_public_access   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  StoredProcedureJob


#### Import instructions
	 from ctm_python_client.jobs.database.stored_procedure import StoredProcedureJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  stored_procedure   
	-  parameters   
	-  return_value   
	-  schema   
	-  connection_profile   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  SQLScriptJob


#### Import instructions
	 from ctm_python_client.jobs.database.sql_script import SQLScriptJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  sql_script   
	-  connection_profile   
	-  parameters=None   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  EmbeddedQueryJob


#### Import instructions
	 from ctm_python_client.jobs.database.embedded_query import EmbeddedQueryJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  query   
	-  variables=None   
	-  output_execution_log=None   
	-  autocommit=None   
	-  output_sql_output=None   
	-  sql_output_format=None   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  AgentJob


#### Import instructions
	 from ctm_python_client.jobs.database.mssql.agent import AgentJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  category   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  SSISJob


#### Import instructions
	 from ctm_python_client.jobs.database.mssql.ssis import SSISJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  package_source   
	-  package_name   
	-  config_files   
	-  properties   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  DeleteJob


#### Import instructions
	 from ctm_python_client.jobs.filewatcher.delete import DeleteJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  path   
	-  search_interval   
	-  time_limit   
	-  start_time   
	-  stop_time   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  FWCreateJob


#### Import instructions
	 from ctm_python_client.jobs.filewatcher.create import FWCreateJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  path   
	-  search_interval   
	-  time_limit   
	-  start_time   
	-  stop_time   
	-  minimum_size   
	-  wild_card   
	-  minimal_age   
	-  maximal_age   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  ProcessChainJob


#### Import instructions
	 from ctm_python_client.jobs.sap.bw.process_chain import ProcessChainJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  process_chain_description   
	-  id   
	-  rerun_option   
	-  enable_peridoic_job   
	-  consider_only_overall_chain_status   
	-  retrieve_log   
	-  detect_spawned_job   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  R3CREATEJob


#### Import instructions
	 from ctm_python_client.jobs.sap.r3.create import R3CREATEJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  sap_job_name   
	-  start_condition   
	-  rerun_from_step   
	-  target   
	-  created_by   
	-  steps   
	-  post_job_action   
	-  spool_list_recipient   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  COPYJob


#### Import instructions
	 from ctm_python_client.jobs.sap.r3.copy import COPYJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  sap_job_name   
	-  exec   
	-  target   
	-  job_count   
	-  job_count_specific_name   
	-  new_job_name   
	-  start_condition   
	-  after_event   
	-  after_event_parameters   
	-  rerun_from_point_of_failure   
	-  copy_from_step   
	-  post_job_action   
	-  detect_spawned_job   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  BatchAccountJob


#### Import instructions
	 from ctm_python_client.jobs.azure.batch_account import BatchAccountJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  job_id   
	-  command_line   
	-  append_log   
	-  wallclock   
	-  max_tries   
	-  retention   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  LogicAppsJob


#### Import instructions
	 from ctm_python_client.jobs.azure.logic_apps import LogicAppsJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  logic_app_name   
	-  request_body   
	-  append_log   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  FunctionJob


#### Import instructions
	 from ctm_python_client.jobs.azure.function import FunctionJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  append_log   
	-  function   
	-  function_app   
	-  parameters   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  SqoopJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.sqoop import SqoopJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  sqoop_command   
	-  sqoop_options   
	-  sqoop_archives   
	-  sqoop_files   
	-  pre_commands   
	-  post_commands   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  HDFSCommandsJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.hdfs_commands import HDFSCommandsJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  commands   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  HDFSFileWatcherJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.hdfs_file_watcher import HDFSFileWatcherJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  hdfs_file_path   
	-  min_deteced_size   
	-  max_wait_time   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  MapredStreamingJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.mapred_streaming import MapredStreamingJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  input_path   
	-  output_path   
	-  mapper_command   
	-  reducer_command   
	-  general_options   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  DistCpJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.dist_cp import DistCpJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  target_path   
	-  source_paths   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  HiveJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.hive import HiveJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  hive_script   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  OozieJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.oozie import OozieJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  job_properties_file   
	-  oozie_options   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  MapReduceJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.map_reduce import MapReduceJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  program_jar   
	-  main_class   
	-  arguments   
	-  pre_commands   
	-  post_commands   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  PigJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.pig import PigJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  pig_script   
	-  parameters   
	-  pre_commands   
	-  post_commands   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  TajoQueryJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.tajo.query import TajoQueryJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  open_query   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  InputFileJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.tajo.input_file import InputFileJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  full_file_path   
	-  parameters=None   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  PythonJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.spark.python import PythonJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  spark_script   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  ScalaJavaJob


#### Import instructions
	 from ctm_python_client.jobs.hadoop.spark.scala_java import ScalaJavaJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  program_jar   
	-  main_class   
	-  arguments   
	-  pre_commands   
	-  post_commands   
	-  spark_options   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  LambdaJob


#### Import instructions
	 from ctm_python_client.jobs.aws.aws_lambda import LambdaJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  function_name   
	-  version   
	-  payload   
	-  append_log_to_output   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  BatchJob


#### Import instructions
	 from ctm_python_client.jobs.aws.batch import BatchJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  job_definition   
	-  job_definition_revision   
	-  job_queue   
	-  aws_job_type   
	-  array_size   
	-  depends_on   
	-  command   
	-  memory   
	-  v_c_p_us   
	-  job_attempts   
	-  execution_timeout   
	-  append_log_to_output   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

#  StepFunctionJob


#### Import instructions
	 from ctm_python_client.jobs.aws.step_function import StepFunctionJob
#### Parameters for the Job constructor 
    parameters having '=None' are optional
	-  folder   
	-  job_name   
	-  connection_profile   
	-  state_machine   
	-  execution_name   
	-  input   
	-  append_log_to_output   
	-  host=None   
	-  run_as=None   
	-  description=None   
 
 
 
<br/>
<br/>

