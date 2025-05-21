# Componentes de Arquitetura do Azure

## 🏗️ Visão Geral

O Azure organiza recursos em uma hierarquia: **Regiões** → **Zonas de Disponibilidade** → **Grupos de Recursos** → **Recursos Individuais**. Cada camada oferece níveis diferentes de isolamento, redundância e organização.

## 🌍 Regiões e Zonas de Disponibilidade

### Regiões
Localização geográfica com um ou mais datacenters. Impacta:
- **Latência**: Escolha próxima aos usuários
- **Custo**: Preços variam por região
- **Compliance**: Alguns dados devem ficar em países específicos

### Zonas de Disponibilidade
Datacenters separados fisicamente dentro da mesma região (2-100km de distância). Protegem contra falhas de datacenter individual.

**SLA**: 99.99% para recursos distribuídos entre zonas vs 99.9% para recursos em zona única.

## 📁 Grupos de Recursos

Containers lógicos que agrupam recursos relacionados. Características:
- Todo recurso pertence a exatamente um grupo
- Excluir o grupo exclui todos os recursos dentro dele
- Aplicação de políticas, permissões e orçamentos unificados

**Estratégias comuns**: Por ambiente (dev/test/prod), por projeto, ou por departamento.

## 🔐 Azure Active Directory (AAD)

Sistema central de identidade que autentica usuários e controla acesso a recursos. Recursos principais:
- **Single Sign-On**: Uma autenticação para múltiplas aplicações
- **Autenticação Multifator**: Verificação adicional de segurança
- **Acesso Condicional**: Regras baseadas em contexto (localização, dispositivo)

## 🌐 Redes Virtuais (VNets)

Redes privadas isoladas onde recursos se comunicam. Componentes:
- **Subnets**: Segmentos dentro da VNet para organizar recursos
- **NSGs**: Regras de firewall para controlar tráfego
- **Conectividade**: VPN Gateway, ExpressRoute, ou Peering entre VNets

## 💾 Contas de Armazenamento

Serviço fundamental de storage com múltiplos tipos:
- **Blob Storage**: Objetos grandes (imagens, vídeos, backups)
- **File Storage**: Compartilhamentos de arquivos
- **Table Storage**: Dados estruturados simples
- **Queue Storage**: Mensagens entre aplicações

**Replicação automática** garante durabilidade dos dados em múltiplas localizações.

## 🎛️ Azure Resource Manager (ARM)

Camada de gerenciamento que coordena todos os recursos:
- **Templates**: Infraestrutura como código (JSON/Bicep)
- **Resource Groups**: Organização e ciclo de vida
- **Políticas**: Regras automáticas de compliance
- **Locks**: Proteção contra exclusões acidentais

## 🔍 Monitoramento (Azure Monitor)

Sistema de observabilidade completo:
- **Métricas**: CPU, memória, rede de recursos
- **Logs**: Log Analytics para consultas complexas
- **Application Insights**: Performance de aplicações
- **Alertas**: Notificações baseadas em condições

## 🔗 Integração e Conectividade

### Service Bus
Messaging confiável entre serviços, garantindo entrega mesmo com falhas temporárias.

### Azure Functions
Código que executa automaticamente em resposta a eventos, sem gerenciar servidores.

### Logic Apps
Fluxos de trabalho visuais para integrar sistemas e automatizar processos.

## ⚡ Padrões Arquiteturais Comuns

### Alta Disponibilidade
- Distribua recursos entre múltiplas zonas
- Use Load Balancers para distribuição de tráfego
- Implemente health checks automáticos

### Segurança em Camadas
- **Rede**: NSGs e firewalls
- **Identidade**: AAD com MFA
- **Aplicação**: Criptografia e secrets management
- **Dados**: Encryption at rest e in transit

### Escalabilidade
- **Auto Scaling**: Ajuste automático baseado em demanda
- **Load Balancing**: Distribuição de carga
- **Caching**: Redis para performance

## 📚 Próximos Passos

1. **Hands-on**: Crie recursos básicos (VM, Storage, VNet)
2. **Templates**: Aprenda ARM/Bicep para automação
3. **Monitoring**: Configure alertas para recursos críticos
4. **Well-Architected Framework**: Estude os 5 pilares da Microsoft

## 🔗 Recursos Úteis

- **Microsoft Learn**: Tutoriais gratuitos estruturados
- **Architecture Center**: Padrões e soluções referenciais
- **Azure Docs**: Documentação técnica detalhada
