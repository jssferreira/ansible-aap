# README TEMPLATE

Bem vindo aos passos para subir uma imagem customizada no Ansible Automation Platform utilizando o Automation Hub.

## Comandos utilizados

Para criar a nova imagem, utilizando os arquivos "execution-environment.yml" e "requirements.yml", utilize os comandos abaixo: 

- podman login -u=user -p=password automation-hub.url.local
- ansible-builder create
- podman tag localhost/custom-ee-mysql:latest hub01.joaosfe.local/custom-ee-mysql:1.0
- podman push hub01.joaosfe.local/custom-ee-mysql:1.0 
