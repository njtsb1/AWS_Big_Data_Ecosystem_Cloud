Daily Learning

# Building a Big Data Ecosystem in the AWS Cloud

Project developed at Bootcamp Cognizant Cloud Data Engineer whit guidance from expert [Cassiano Peres](https://github.com/cassianobrexbit/ "Cassiano Peres").</br>
Learning to Work with the word counter algorithm. Ordering the words by occurrence and not by alphabetical order (presenting the most cited in the text with priority), for example.
(Aprendendo a trabalhar com  algoritmo contador de palavras. Ordenando as palavras por ocorrência e não por ordem alfabética (apresentando as mais citadas no texto com prioridade), por exemplo.)

[LICENSE](/LICENSE)

See [original repository](https://github.com/cassianobrexbit/DIO-LiveCoding-AWS-BigData).

## Instructions

* Access S3: [https://s3.console.aws.amazon.com/s3/](https://s3.console.aws.amazon.com/s3/)
  * Create data lake structure : _dio-live-datalake_
  * Create folder structure:
    * _date_
    * _output_
    * _temp_
* Access EMR: [https://console.aws.amazon.com/elasticmapreduce/](https://console.aws.amazon.com/elasticmapreduce/)
  * The cluster will be created by MrJob and not by the console
  * Infrastructure as code
* Create SSH key
  * Access EC2 Console: [https://console.aws.amazon.com/ec2/](https://console.aws.amazon.com/ec2/) -> Key Pairs -> Create Key Pair
  * Download .pem file
* Get AWS Id and secret key to configure MrJob
  * Profile
  * My Security Credentials: [https://console.aws.amazon.com/iam/home?region={region}#/security_credentials]
  * Access Keys - Create new access key
  * Download - only chance to preview
* Linux environment
  * Create python virtual environment: _virtualenv --python=python3.6 venv_diolive_
  * Access with vs code
* Install vscode on Ubuntu
  * code .
* Create word analysis algorithm
  * dio-live-wordcount-test.py
  * map-reduce-count : count
  * Install boto3: _pip install boto3_
  * Install mrjob: _pip install mrjob_
* Access S3
  * Upload file to bucket
* Python virtual environment: source venv_teste/bin/activate
  * _nano ~/.mrjob.conf_
  * _python3 dio-live-wordcount-test.py -r emr s3://{your_s3_bucket_name}/data/SherlockHolmes.txt --output-dir=s3://{your_s3_bucket_name}/output/logs1 --cloud-tmp- dir=s3://{your_s3_bucket_name}/temp/_
