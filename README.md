# 🛠️ Script de Configuração de Ambiente Linux

## 📄 Descrição

Este script Bash automatiza a criação de diretórios, grupos de usuários, usuários e a configuração de permissões em um sistema Linux. É ideal para ambientes corporativos ou educacionais onde é necessário segmentar o acesso entre diferentes departamentos.

## 📁 Estrutura Criada

- `/publico` - Acesso liberado para todos os usuários.
- `/adm` - Acesso exclusivo para o grupo `GRP_ADM`.
- `/ven` - Acesso exclusivo para o grupo `GRP_VEN`.
- `/sec` - Acesso exclusivo para o grupo `GRP_SEC`.

## 👥 Grupos Criados

- `GRP_ADM` - Administradores
- `GRP_VEN` - Vendedores
- `GRP_SEC` - Segurança

## 👤 Usuários Criados

### Grupo ADM:
- carlos
- maria
- joao

### Grupo VEN:
- debora
- sebastiana
- roberto

### Grupo SEC:
- josefina
- amanda
- rogerio

Todos os usuários são criados com o shell `/bin/bash` e senha padrão: `Senha123` (criptografada via `openssl`).

## 🔐 Permissões

- Diretórios `/adm`, `/ven` e `/sec` possuem permissão `770`, garantindo acesso apenas aos usuários do grupo.
- Diretório `/publico` também com `770`, mas pode ser ajustado para `777` se desejar acesso geral.

## 🚀 Como Usar

1. Salve o script como `setup.sh`.
2. Dê permissão de execução:  
   ```bash
   chmod +x setup.sh
   
## Execute como root:
```bash   
   sudo ./setup.sh

## ⚠️ Observações
O script sobrescreve os usuários caso já existam.

Modifique o script conforme necessário para o seu ambiente (senhas, shells, permissões etc.).

