# 🚀 Dchat - Ct Enterprise Unlocker

Script para desbloquear funcionalidades enterprise do Ct, removendo limitações da versão community.

## ⚡ Uso Rápido

Execute diretamente no container do Chatwoot:

```bash
wget -qO- https://raw.githubusercontent.com/LuizBranco-ClickHype/Dchat/main/unlock.rb | bundle exec rails runner -
```

## 🎯 O que o script faz

### ✅ Configurações do Banco de Dados
- Define o plano como `enterprise`
- Configura limite de usuários para 9.999.999
- Remove alertas de limitação do Redis

### ✅ Atualização de Fallbacks
- Modifica `lib/chatwoot_hub.rb`
- Cria backup automático do arquivo original
- Atualiza valores padrão para enterprise

## 🔧 Funcionalidades Desbloqueadas

Após executar o script, seu Chatwoot terá:

- 🔓 **Usuários ilimitados** (9.999.999)
- 🏢 **Funcionalidades enterprise** ativadas
- 🚫 **Sem alertas** de limitação
- 💾 **Configurações persistentes**

## 📝 Detalhes Técnicos

### Arquivos Modificados
- `installation_configs` (banco de dados)
- `lib/chatwoot_hub.rb` (fallbacks)
- Cache Redis (limpeza de alertas)

### Configurações Aplicadas
```ruby
INSTALLATION_PRICING_PLAN = 'enterprise'
INSTALLATION_PRICING_PLAN_QUANTITY = 9999999
```

### Backups Automáticos
O script cria backups automáticos antes de modificar arquivos:
```
lib/chatwoot_hub.rb.backup.YYYYMMDD_HHMMSS
```

## 🐳 Compatibilidade

- ✅ Container Docker do Ct
- ✅ Instalações Rails padrão
- ✅ Versões recentes do Ct

## ⚠️ Importante

Este script modifica configurações do Chatwoot para remover limitações comerciais. Use de acordo com os termos de licença do software.

## 🔄 Após a Execução

1. Reinicie o container do Ct
2. Acesse a interface web
3. Verifique se as limitações foram removidas

## 👨‍💻 Autor

**Dchat** desenvolvido por **LuizBranco-ClickHype**

---

### 🌟 Repositório: [LuizBranco-ClickHype/Dchat](https://github.com/LuizBranco-ClickHype/Dchat)
