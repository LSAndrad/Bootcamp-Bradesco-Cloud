# Laboratório Azure: Criação e Configuração de Máquinas Virtuais

## 📋 Objetivo do Laboratório

Este repositório documenta o aprendizado prático sobre **criação e configuração de máquinas virtuais no Microsoft Azure**. Serve como guia de referência pessoal com resumos, anotações e dicas descobertas durante a experiência hands-on com a plataforma.

## 🎯 O que são Máquinas Virtuais no Azure

Uma máquina virtual (VM) no Azure é como alugar um computador completo que roda nos datacenters da Microsoft. Você obtém processamento, memória, armazenamento e conectividade sem precisar comprar ou manter hardware físico.

**Analogia**: É como morar em um apartamento mobiliado onde toda a infraestrutura já está pronta para uso, você só precisa se mudar e começar a trabalhar.

## ⚙️ Planejamento: Decisões Antes de Criar

### Sistema Operacional
- **Windows VMs**: Ideais para aplicações Microsoft, SQL Server, .NET
- **Linux VMs**: Mais econômicas, ótimas para web servers e containers

### Dimensionamento das VMs
- **Série B**: Para uso intermitente, sites pequenos, desenvolvimento
- **Série D**: Equilíbrio geral, maioria das aplicações empresariais  
- **Série E**: Otimizadas para aplicações que precisam de muita memória

### Localização Geográfica
Escolha a região mais próxima dos seus usuários. No Brasil, use "Brazil South" (São Paulo) para melhor performance.

## 🔧 Processo de Criação Passo a Passo

### 1. Configurações Básicas
- **Grupo de Recursos**: Use nomes descritivos como "projeto-ecommerce-producao"
- **Nome da VM**: Escolha nomes identificáveis como "vm-web-producao-01"
- **Região**: Prefira regiões próximas aos usuários finais

### 2. Autenticação
- **Por senha**: Mais simples, mas menos segura
- **Por chave SSH**: Muito mais segura, recomendada para produção

### 3. Configuração de Rede
- **Rede Virtual**: O "bairro privado" onde sua VM vai residir
- **Subnet**: O "quarteirão" dentro da rede virtual
- **IP Público**: Necessário apenas se a VM deve ser acessível da internet

### 4. Segurança
**Grupos de Segurança de Rede (NSGs)** funcionam como firewalls que controlam o tráfego. Configure regras específicas como "permitir web (porta 80)" ou "permitir SSH apenas de IPs específicos".

## 🚀 Configuração Pós-Criação

### Primeiro Acesso
- **Linux**: Use SSH através do terminal
- **Windows**: Use Remote Desktop Protocol (RDP)

### Tarefas Essenciais
1. **Atualizações de sistema**: `sudo apt update && sudo apt upgrade` (Ubuntu)
2. **Instalação de software**: Configure apenas o necessário para sua aplicação
3. **Backup inicial**: Configure antes de colocar em produção

## 💡 Dicas Importantes e Lições Aprendidas

### Gerenciamento de Custos
- **Desligue corretamente**: Use "Deallocate" no portal, não apenas "Stop" no sistema operacional
- **Monitore gastos**: Configure alertas de custo no Azure
- **Tamanho adequado**: Comece pequeno, você pode aumentar depois

### Segurança
- **Sempre use chaves SSH** para Linux em produção
- **Configure NSGs restritivos**: Permita apenas o tráfego necessário
- **Mantenha sistema atualizado**: Configure atualizações automáticas quando possível

### Backup e Monitoramento  
- **Configure backup automático** desde o primeiro dia
- **Monitore métricas básicas**: CPU, memória, disco
- **Documente tudo**: Anote cada configuração para facilitar replicação

## ⚠️ Armadilhas Comuns para Iniciantes

**Custos inesperados**: VMs "stopped" ainda geram custos de armazenamento. Use "Deallocate" para parar completamente.

**Segurança inadequada**: Nunca deixe portas abertas desnecessariamente. SSH na porta 22 deve ser restrito a IPs conhecidos.

**Backup negligenciado**: Não espere ter problemas para configurar backup. Murphy's Law sempre se aplica em TI.

## 📚 Próximos Passos para Evolução

### Conceitos Intermediários
- **Extensões de VM**: Adicione funcionalidades automaticamente
- **Discos gerenciados**: Entenda diferenças de performance e confiabilidade
- **Load Balancers**: Para distribuir carga entre múltiplas VMs

### Automação
- **ARM Templates**: Defina infraestrutura como código
- **Azure CLI**: Automatize tarefas repetitivas
- **Scripts**: PowerShell ou Bash para configurações padronizadas

## 🔗 Recursos para Aprendizado Contínuo

**Documentação Oficial**: Microsoft Learn oferece tutoriais gratuitos e detalhados

**Laboratórios Práticos**: Use o sandbox do Microsoft Learn para experimentar sem custos

**Comunidade**: Stack Overflow, Reddit r/AZURE, Microsoft Tech Community para dúvidas e discussões

---

## 📝 Anotações Pessoais

*Seção reservada para anotações específicas do laboratório, comandos úteis descobertos, configurações personalizadas testadas, e observações sobre performance em diferentes cenários.*

---

**💭 Reflexão**: Este material representa o conhecimento base adquirido. A tecnologia evolui rapidamente, então este documento será atualizado conforme novas experiências e aprendizados forem acumulados.
