## Setup básico inicial
- Rodar o Kali no VirtualBox

```bash
 sudo apt update; apt dist-upgrade
```

### Configurar SSH

1. Entrar como root

```bash	
sudo su
passwd root
```

2. Habilitar o serviço SSH

```bash
systemctl enable ssh
systemctl start ssh
# conferir o status do serviço SSH
systemctl status ssh
```

3. Pegar o IP da máquina

```bash
ip a s | grep inet
```

4. Conectar via SSH

```bash
ssh root@<ip>
```

5. Verificar se a porta 22 está aberta na máquina

- IPV4 e IPV6

```bash
netstat -tpan | grep 22
```