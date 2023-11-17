# sprint-5-desafio-2
<h1><strong>Instalar o terraform no seu desktop e criar o deploy de uma instancia EC2 t2.micro na AWS</strong></h1>
<br>
<strong>Passo 1: Instalar o Terraform</strong>
<br><br>

Baixe o Terraform:
<br>
    Visite o site oficial do Terraform em https://www.terraform.io/downloads.html e baixe a versão adequada para o seu sistema operacional.
<br>
    Descompacte o arquivo baixado:
    <br>
    Após o download, descompacte o arquivo em um diretório de sua escolha.
<br>
    Adicione o diretório ao PATH:
    <br>
    Adicione o caminho para o diretório do Terraform ao seu PATH para facilitar o acesso aos comandos. Isso geralmente é feito configurando a variável de ambiente PATH.
<br><br>
Passo 2: Criar o arquivo de configuração
<br>
Crie um arquivo chamado, por exemplo, main.tf para conter a configuração do Terraform.
<br>
# main.tf
<br>
provider "aws" {
<br>
  region = "us-east-1"  # Troque para a região desejada
  <br>
}
<br>
resource "aws_instance" "example" {
<br>
  ami           = "ami-0c55b159cbfafe1f0"  # AMI da região desejada
  <br>
  instance_type = "t2.micro"
  <br>

  tags = {
  <br>
    Name = "ExemploEC2"
    <br>
  }
  <br>
}
<br>
Passo 3: Inicializar e aplicar as configurações
<br>
    Abra um terminal e navegue até o diretório onde você salvou o arquivo main.tf.
<br>
    Execute o comando terraform init para inicializar o diretório de trabalho.
<br>
O Terraform solicitará confirmação para criar os recursos. Digite yes e pressione Enter.
<br>
Após a conclusão do apply, o Terraform mostrará informações sobre os recursos criados.
