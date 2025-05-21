# Dimensionamento de VMs no Azure

## 🎯 O que é?

**Auto Scaling**: Azure adiciona ou remove VMs automaticamente baseado na demanda

## ⚙️ Configuração Básica

Crie um **VM Scale Set** com:
- Mínimo: 2 VMs
- Máximo: 10 VMs  
- Padrão: 3 VMs

## 📊 Regras de CPU

### Adicionar VMs
- CPU > 70% por 5 minutos → +1 VM

### Remover VMs  
- CPU < 25% por 10 minutos → -1 VM

## ⏱️ Tempo de Espera

- **5 minutos** entre cada ação de scaling
- Evita mudanças muito rápidas

## 💻 Tipos de VM

| Série | Para que usar | Exemplo |
|-------|---------------|---------|
| B | Sites pequenos | B2s |
| D | Aplicações gerais | D2s_v3 |
| E | Muita memória | E2s_v3 |
| F | Processamento pesado | F2s_v2 |

## 🔧 Como Configurar

1. Portal Azure → VM Scale Sets
2. Criar novo scale set
3. Configurar → Scaling 
4. Adicionar regras de CPU
5. Testar com carga

## 💰 Economizar

- **Reserved Instances**: Para VMs 24/7
- **Spot VMs**: Para teste/desenvolvimento  
- **Auto-shutdown**: Desligar à noite

## ⚠️ Dicas

- Teste antes de produção
- CPU 70% melhor que 90%
- Monitore os custos
- Configure alertas
