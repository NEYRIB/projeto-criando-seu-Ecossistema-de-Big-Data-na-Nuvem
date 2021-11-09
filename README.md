# Criando seu Ecossistema de Big Data na Nuvem
Repositório com instruções sobre AWS EMR e Python

Neste repositório há os arquivos de configuração e execução de análise de dados.

Usamos como base o DIO-LiveCoding-AWS-BigData com Cassiano Peres Instrutor, Digital Innovation One

## Prática 1: Explorando Alguns Serviços/Ferramentas

* Acessar

https://aws.amazon.com/pt/?nc2=h_lg

Serviços da AWS

Documentação da Amazon para leitura

Login Console

Todos os serviços

https://aws.amazon.com/pt/console/

AWS Services

Serviços de Big Data

Serviços de análise da AWS

Explorar e estudar Amazon EMR (Estrutura Hadoop Hospedada)

# Prática 2: Visão Geral sobre a Arquitetura do Desafio

* Objetivo;

Implementar um cluster para processamento distribuído de dados utilizando o serviço AWS EMR com o  Haddop MapReduce MapReduce (FrameWork (Jobs)) para contar palavras em um arquivo de texto (Livro Sherlock Holmes)  armazenado no AWS S3, através de um algoritmo em Python.

![image](https://user-images.githubusercontent.com/88436657/140667838-25cae859-4a3f-4c72-946b-54e7841d5bd2.png)

# Prática 2: Configurando o S3 e EC2 na AWS

Login “AWS Management Console”

![image](https://user-images.githubusercontent.com/88436657/140668233-6a6fc0c7-57a2-4a0f-84b6-20b2565e1b0c.png)

Serviço EMR
![image](https://user-images.githubusercontent.com/88436657/140668301-f55630eb-fab4-4a37-b341-04af55e49ef5.png)
Criação de Cluster

Terminal do Linux Power Shell
![image](https://user-images.githubusercontent.com/88436657/140668334-e0085f79-0035-4f19-9d43-c5d2f91a4a7c.png)

Acessar S3

Criar Buckets
![image](https://user-images.githubusercontent.com/88436657/140668481-8ace8bcb-35f0-4b3c-965e-2177a3b4e6b3.png)
![image](https://user-images.githubusercontent.com/88436657/140668492-8d9389b7-5ec1-4b93-b2fb-b15abfe5d0ab.png)

Instruções do Professor;

* Acessar S3: https://s3.console.aws.amazon.com/s3/ 
  * Criar estrutura de data lake : _dio-live-datalake_
  * Criar estrutura de pastas:
    * _data_
    * _output_
    * _temp_
    
* Acessar EMR: https://console.aws.amazon.com/elasticmapreduce/
    * O cluster será criado pelo MrJob e não pelo console
    * Infraestrutura como código 
* Criar chave SSH
    * Acessar  Console do EC2: https://console.aws.amazon.com/ec2/ -> Key Pairs -> Create Key Pair	
    * Download .pem file
* Obter Id e chave secreta AWS para configurar MrJob
   * Profile
   * My Security Credentials: https://console.aws.amazon.com/iam/home?region={region}#/security_credentials
   * Access Keys - Create new access key
   * Fazer download - única chance de visualizar

![image](https://user-images.githubusercontent.com/88436657/141016025-03a04db5-dc35-478d-98e4-36404429310d.png)


* Ambiente linux
   * Criar ambiente virtual python: _virtualenv --python=python3.6 venv_diolive_
   * Acessar com o vs code
* Instalar vscode no Ubuntu
   *  code .
* Criar algoritmo de análise de palavras
   * dio-live-wordcount-test.py
   * map-reduce-count : contar
   * Instalar boto3: _pip install boto3_
   * Instalar mrjob: _pip install mrjob_
* Acessar S3
   * Upload de arquivo para o bucket
* Ambiente virtual python: source venv_teste/bin/activate
  * _nano ~/.mrjob.conf_
  * _python3 dio-live-wordcount-test.py -r emr s3://{your_s3_bucket_name}/data/SherlockHolmes.txt --output-dir=s3://{your_s3_bucket_name}/output/logs1 --cloud-tmp-dir=s3://{your_s3_bucket_name}/temp/_

![image](https://user-images.githubusercontent.com/88436657/141016703-51cab614-30dc-4669-a9f1-a226f1818a66.png)


![image](https://user-images.githubusercontent.com/88436657/141016769-59f9b9b4-687b-4ec5-9bac-cd753d28cf82.png)

![image](https://user-images.githubusercontent.com/88436657/141016818-63396380-37d9-4654-abcf-1633cde49eff.png)

![image](https://user-images.githubusercontent.com/88436657/141016866-16ed8d94-6a8d-4dcd-9122-23e1b7bbc9ad.png)

