# Configuração de chave RSA no Git

- [Criação Chave RSA](#instalação-nfs-server-no-centos)
- [Configuração da Chave RSA no Git](#primeiro-passo-corrigir-o-horário-do-servidor)
- [Replicação de chave RSA nos servidores](#ajustes-de-so-após-a-instalação)



### 1º Passo - Gerar chave RSA

```bash
ssh-keygen -t rsa -b 4096
```

#### 2º Passo - Inserir a chave RSA no repositorio

```bash
No repositorio GIT, acesse Settings > Deploy Keys
Insira a chave id_rsa.pub
```

#### 3º Passo - Copiar a chave Privada para outros servidores

```bash
rsync -avz /root/.ssh/* root@172.0.0.102:/root/.ssh/
```
