# 📘 Glossário de Padrões de Arquitetura e Design

Este documento reúne os principais padrões de arquitetura e design de software, suas características, exemplos de uso e fontes de referência.

---

## 📂 Índice
- [Arquiteturas](#arquiteturas)
- [Padrões de Design](#padrões-de-design)
- [Extensões Arquiteturais](#extensões-arquiteturais)
- [Anti-patterns](#anti-patterns)
- [Referências](#referências)

---

## 🏛️ Arquiteturas

| Termo | Definição | Características Principais | Exemplo de Uso |
|-------|-----------|----------------------------|----------------|
| **Monolith** | Sistema de componente único sem modularidade interna. | Alta coesão, baixa latência, fácil depuração, baixa flexibilidade. | Protótipos rápidos, sistemas pequenos ou legados. |
| **Microsserviços** | Segmenta o sistema em serviços independentes que se comunicam por APIs. | Escalabilidade granular, implantação independente, poliglota. | Netflix, grandes e-commerces. |
| **CQRS** | Segrega comandos (escrita) e consultas (leitura). | Consistência eventual, escalabilidade assimétrica. | E-commerces com modelos distintos de leitura e transação. |
| **Hexagonal Architecture** | Isola lógica de negócio de dependências externas. | Independência de frameworks, facilita testes. | Adaptadores para múltiplos bancos de dados. |
| **Service Mesh** | Camada para gerenciar comunicação e segurança entre serviços. | mTLS nativo, proxies sidecar, controle granular. | Istio, Linkerd. |
| **SAGA** | Gerencia transações distribuídas com ações compensatórias. | Consistência eventual, orquestração ou coreografia. | Reserva de viagem com cancelamentos encadeados. |
| **MVC** | Separa aplicação em Modelo, Visão e Controlador. | Modularidade, separação de responsabilidades. | Interfaces web. |
| **SOA** | Usa serviços para criar aplicações de negócios. | Interoperabilidade, acoplamento fraco. | Integração de sistemas legados de saúde. |
| **Layers (n-tier)** | Divide sistema em camadas lógicas e físicas. | Escalabilidade por camada, manutenção facilitada. | Arquitetura Three-Tier. |
| **Pipeline (Pipes-and-Filters)** | Processamento em sequência de filtros independentes. | Flexibilidade, modularidade. | ETL, análise de spam. |
| **EDA (Event-Driven Architecture)** | Baseado em produção e consumo de eventos. | Escalabilidade independente, processamento assíncrono. | Notificação de estoque/logística em pedidos. |
| **Onion Architecture** | Padrão centrado no domínio. | Independência de frameworks, foco no núcleo. | Aplicações de longo prazo. |

---

## 🎨 Padrões de Design

| Termo | Categoria | Definição | Exemplo |
|-------|-----------|-----------|---------|
| **Singleton** | Criacional | Garante instância única. | Configuração global, pool de conexões. |
| **Factory Method** | Criacional | Cria objetos sem especificar classe exata. | Fábricas de formas geométricas. |
| **Adapter** | Estrutural | Converte interfaces incompatíveis. | Integração de sistemas legados. |
| **Facade** | Estrutural | Interface simplificada para subsistemas complexos. | Abstração de sistema de arquivos. |
| **Proxy** | Estrutural | Intermediário que controla acesso. | Reverse Proxy (Nginx). |
| **Strategy** | Comportamental | Define família de algoritmos intercambiáveis. | Estratégias de desconto. |
| **Observer** | Comportamental | Dependência um-para-muitos com notificações. | Notificação de novos produtos. |
| **State** | Comportamental | Altera comportamento conforme estado interno. | Status de pedidos. |

---

## ☁️ Padrões Cloud e Messaging

| Termo | Definição | Exemplo |
|-------|-----------|---------|
| **Event Sourcing** | Estado armazenado como sequência de eventos imutáveis. | Rastreamento de pedidos no Cosmos DB. |
| **Circuit Breaker** | Evita falhas em cascata interrompendo chamadas instáveis. | Serviços de pagamento instáveis. |
| **Sidecar** | Componente auxiliar anexado à aplicação principal. | Contêiner `daprd` do Dapr. |
| **Ambassador** | Serviços auxiliares que enviam solicitações em nome do cliente. | Proxies em Service Mesh. |
| **Queue-Based Load Leveling** | Usa fila como buffer para nivelar carga. | Azure Service Bus. |
| **Claim-Check** | Divide mensagem grande em referência e payload externo. | Blob Storage + barramento de mensagens. |

---

## 🔧 Extensões Arquiteturais

| Termo | Definição | Exemplo |
|-------|-----------|---------|
| **Shared Repository** | Banco central compartilhado por múltiplos componentes. | Inventário em SQL central. |
| **Orchestrator** | Serviço que integra outros serviços. | Saga Orchestrator em pedidos/pagamentos. |
| **Shards** | Divide carga em múltiplas instâncias independentes. | Servidores de chat por grupos de usuários. |

---

## ⚠️ Anti-patterns

| Termo | Definição | Exemplos |
|-------|-----------|----------|
| **Anti-patterns** | Estratégias comuns mas ineficazes. | *God Object*, *Big Ball of Mud*. |

---

## 📎 Referências

1. *The Pattern Language of Software Architecture - GitHub*  
2. *Arquitetura de software: guia, objetivos e quando contratar*  
3. *Padrões arquiteturais: arquitetura de software descomplicada - Alura*  
4. *The Azure Cloud Native Architecture Mapbook - Microsoft .NET*  
5. *CQRS Pattern - Azure Architecture Center | Microsoft Learn*  
6. *Service Mesh Architecture - Solo.io*  
7. *Patterns in Microservices-based Development: A Grey Literature Review*  
8. *SOA – AWS*  
9. *Anti-pattern - Wikipedia*  
10. *Design Patterns - Wikipedia*  
11. *Comparison between Layered, N-Tier, and Onion Architecture - ITNEXT*  
12. *EDA – AWS*  
13. *SOLID Design Principles - DEV Community*  
14. *Gang of Four Design Patterns - Rose-Hulman*  
15. *Design Patterns in Python - Alex Martelli*  
16. *Observer - Refactoring.Guru*  
17. *Software Architecture Patterns - The Swiss Bay*  
18. *eda-visuals-v0.0.34.pdf - David Boyne*  
