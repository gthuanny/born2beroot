# born2beroot

Projeto de **System Administration** da 42 com foco em virtualização, segurança e configuração de um servidor Linux utilizando Debian (versão estável).

---

## 📌 Objetivo

Configurar uma máquina virtual segura com:

- Debian (instalação mínima, sem interface gráfica)
- Particionamento manual
- LVM criptografado (LUKS)
- SSH seguro na porta 4242
- Firewall ativo
- Política de senha forte
- Script de monitoramento em bash

---

## 🖥️ Ambiente

| Componente | Configuração |
|------------|-------------|
| SO | Debian (stable) |
| Virtualização | VirtualBox |
| Interface gráfica | ❌ Não instalada |
| SSH | Porta 4242 |
| Firewall | UFW ativo |
| Usuário | `<login>` + grupos `sudo` e `user42` |

---

## 🔐 Particionamento

Estrutura obrigatória com `/boot` separado e LVM criptografado:

# 🛠 Born2BeRoot — Comandos para Correção

---

## 🔎 Text Compare

https://text-compare.com/

---

# 🖥 Sistema & Ambiente

## 🚫 Verificar ausência de interface gráfica
```bash
ls /usr/bin/*session
```

---

## 🐧 Informações do Sistema Operacional
```bash
uname -v
uname --kernel-version
```

---

## 🏷 Hostname
```bash
hostname
```

### Alterar hostname
```bash
sudo nano /etc/hostname
sudo nano /etc/hosts
```

Reiniciar:
```bash
sudo reboot
```

---

# 👤 Usuários & Grupos

## Ver grupos
```bash
getent group sudo
getent group user42
```

## Criar usuário
```bash
sudo adduser <nome>
```

## Criar grupo
```bash
sudo addgroup <nome>
```

## Adicionar usuário a grupo
```bash
sudo adduser <user> <group>
```

## Verificar grupo
```bash
getent group <group>
```

---

# 🔐 SUDO

## Verificar instalação
```bash
which sudo
dpkg -s sudo
```

## Adicionar usuário ao sudo
```bash
sudo adduser <name> sudo
getent group sudo
```

## Configuração personalizada
```bash
sudo nano /etc/sudoers.d/sudo_config
```

## Caminho e logs do sudo
```bash
cd /var/log/sudo
ls
cat sudo_config
sudo nano lmao
cat sudo_config
```

---

# 🔥 UFW (Firewall)

## Verificar instalação
```bash
dpkg -s ufw
```

## Status do firewall
```bash
sudo ufw status
sudo service ufw status
```

## Listar regras numeradas
```bash
sudo ufw status numbered
```

## Criar regra
```bash
sudo ufw allow 8080
```

## Remover regra
```bash
sudo ufw status numbered
sudo ufw delete <num_rule>
sudo ufw status numbered
sudo ufw delete <num_rule>
sudo ufw status numbered
```

---

# 🔑 SSH

## Verificar instalação
```bash
which ssh
```

## Status do serviço
```bash
sudo service ssh status
```

## Conectar via SSH
```bash
ssh root@localhost -p 4241
ssh <new_user>@localhost -p 4241
```

---

# 💾 Partições
```bash
lsblk
```

---

# 📊 Monitoramento (Cron)

## Editar cron do root
```bash
sudo crontab -u root -e
```

## Reiniciar serviço cron
```bash
sudo /etc/init.d/cron stop
sudo /etc/init.d/cron start
```

---

@gde-cast 42 Porto
