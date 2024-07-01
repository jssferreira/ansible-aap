# README TEMPLATE

Bem vindo! Siga os passos abaixo para subir uma imagem customizada no Ansible Automation Platform utilizando o Automation Hub.

## Customizando o ambiente

É possível utilizar uma imagem base para subir uma nova, editando o arquivo "execution-environment.yml", informando a imagem que deseja utilizar do seu Automation Hub ou diretamente da Red Hat, disponibilizada no registry.redhat.io.
Além disso, para instalar os módulos customizados do ansible que irá utilizar na imagem, você deve informá-los no arquivo "requirements.yml".

Referências: <br/>
<a href="https://docs.ansible.com/automation-controller/latest/html/userguide/execution_environments.html" target="_blank">Execution Environment</a><br/>
<a href="https://www.redhat.com/sysadmin/ansible-execution-environment-unconnected" target="_blank">Build execution environment images</a>


## Comandos utilizados

Para criar a nova imagem, utilizando os arquivos "execution-environment.yml" e "requirements.yml", utilize os comandos abaixo: 

- podman login -u=user -p=password automation-hub.url.local
- ansible-builder create
- podman tag localhost/custom-ee-mysql:latest hub01.joaosfe.local/custom-ee-mysql:1.0
- podman push hub01.joaosfe.local/custom-ee-mysql:1.0 
