# Configuração de chave RSA no Git

- [Criação Chave RSA](#Gerar-chave-RSA)
- [Configuração da Chave RSA no Git](#Inserir-a-chave-RSA-no-repositorio)
- [Replicação de chave RSA nos servidores](#Copiar-a-chave-Privada-para-outros-servidores)



### Gerar chave RSA

```bash
ssh-keygen -t rsa -b 4096
```

### Inserir a chave RSA no repositorio

```bash
No repositorio GIT, acesse Settings > Deploy Keys
Insira a chave id_rsa.pub
```

### Copiar a chave Privada para outros servidores

```bash
rsync -avz /root/.ssh/* root@172.0.0.102:/root/.ssh/
```
