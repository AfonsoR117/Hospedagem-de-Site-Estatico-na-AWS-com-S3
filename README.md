# Hospedagem-de-Site-Est-tico-na-AWS-com-S3
Este projeto demonstra como hospedar um site estático utilizando o serviço Amazon S3 da Amazon Web Services.  
O objetivo foi aprender conceitos básicos de computação em nuvem, armazenamento, 
deploy e hospedagem web sem necessidade de servidor físico ou máquina virtual.


# Tecnologia
HTML5
CSS3
AWS
Hospedagem estática
Polícia do Balde
Controle de acesso público


# Objetivo do Projeto

Criar um site simples hospedado na nuvem utilizando apenas serviços serverless da AWS.

Com esse projeto foi possível aprender:

criação de buckets no S3
Enviado por arqu
configuração de hospedagem estática
gerenciamento de permissões
políticas de acesso público
deploy de aplicações web simples



# Estrutura 
/index.html
/style.css


# Funcionamento 

O fluxo da aplicação funciona da seguinte forma:

Usuário → AWS S3 → Site Estático

Os arquivos HTML e CSS são armazenados dentro de um bucket S3 configurado para hospedagem estática.



# Etapas Realizadas 
# 1. Criação do Bucket S3

Foi criado um bucket no AWS S3 para armazenar os arquivos do site.



# 2. Upload dos Arquivos

Os arquivos:

index.html
estilo.css

foram enviados para o bucket.



# 3. Configuração de Static Website Hosting

Foi habilitada a opção:

Static Website Hosting
definindo:

documento de índice →index.html



# 4. Configuração de Permissões

As configurações de bloqueio de acesso público foram ajustadas para permitir acesso ao site.

Também foi criada uma Bucket Policy permitindo leitura pública dos arquivos:

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::testeemsiteestatico/*"
    }
  ]
}


# Resultado

https://testeemsiteestatico.s3.sa-east-1.amazonaws.com/Main.html



# Conceitos Aprendidos

Durante o desenvolvimento deste projeto foram praticados conceitos importantes de cloud computing:

- armazenamento em nuvem
- hospedagem serverless
- deploy de aplicações web
- gerenciamento de permissões
- políticas IAM
- acesso público controlado
- arquitetura estática





















