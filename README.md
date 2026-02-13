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

