# MecanicoSys 2025 — Documento de Requisitos  
Sistema da Oficina **AutoFix+**

---

## 1. Requisitos Funcionais (RF)

| Código | Descrição | Categoria | Usuário |
|:------:|-----------|-----------|---------|
| **RF01** | O sistema deve permitir acesso multiplataforma (web e mobile). | Acesso | Cliente / Atendente / Mecânico |
| **RF02** | O sistema deve permitir o cadastro de clientes com autenticação por e-mail e senha. | Cadastro | Cliente |
| **RF03** | O sistema deve permitir cadastrar veículos associados aos clientes, incluindo dados técnicos. | Cadastro | Atendente |
| **RF04** | O sistema deve permitir abrir uma Ordem de Serviço (OS) vinculada ao cliente e ao veículo. | Processo Operacional | Atendente |
| **RF05** | O sistema deve permitir alterar o status da OS (Recebido, Em Análise, Aguardando Aprovação, Em Serviço, Finalizado, Pronto para Retirada). | Fluxo de Serviço | Mecânico / Atendente |
| **RF06** | O sistema deve permitir o envio de fotos e vídeos do diagnóstico da manutenção. | Evidências Técnicas | Mecânico |
| **RF07** | O sistema deve enviar ao cliente solicitações de aprovação de orçamentos extras via web/app. | Comunicação | Mecânico / Sistema |
| **RF08** | O sistema deve permitir ao cliente aprovar ou rejeitar solicitações de orçamento. | Interação | Cliente |
| **RF09** | O sistema deve enviar notificações automáticas quando o status da OS for alterado. | Comunicação | Cliente |
| **RF10** | O sistema deve exibir ao cliente o histórico de OS com datas, valores, serviços e evidências. | Histórico | Cliente |
| **RF11** | O sistema deve exibir à atendente o histórico completo de serviços da oficina. | Histórico Administrativo | Atendente |
| **RF12** | O sistema deve registrar previsão de entrega obrigatória ao abrir uma OS. | Controle de Processo | Atendente |
| **RF13** | O sistema deve gerar relatórios sobre tempo médio de serviço, peças utilizadas e produtividade. | Relatórios | Gerência |

---

## 2. Requisitos Não Funcionais (RNF)

| Código | Descrição | Categoria |
|:------:|-----------|-----------|
| **RNF01** | O sistema deve possuir interface simples, adequada a usuários com pouca familiaridade com tecnologia (ex.: Seu Jorge). | Usabilidade |
| **RNF02** | O sistema deve operar 24h/7 para consulta de histórico, confirmações e aprovações. | Disponibilidade |
| **RNF03** | As notificações devem ser enviadas em até 5 segundos após mudanças de status. | Desempenho |
| **RNF04** | Dados sensíveis dos clientes devem ser exibidos parcialmente (ex.: CPF 123.***.***-89). | Segurança |
| **RNF05** | O sistema deve ser compatível com Android, iOS e navegadores modernos. | Compatibilidade |
| **RNF06** | A interface deve ter contraste adequado e permitir aumento de fonte. | Acessibilidade |

---

## 3. Regras de Negócio (RN)

| Código | Descrição |
|:------:|-----------|
| **RN01** | Nenhum serviço adicional pode ser realizado sem aprovação explícita do cliente. |
| **RN02** | Solicitações de orçamento expiram automaticamente após **24 horas**. |
| **RN03** | Após expirar o orçamento, será cobrada taxa diária de **R$ 50,00** até nova decisão do cliente. |
| **RN04** | O cliente só pode cancelar enquanto a OS estiver no status **Aguardando Aprovação**. |
| **RN05** | Fotos e vídeos enviados pelo mecânico devem ser anexados permanentemente à OS. |
| **RN06** | Toda OS deve ter previsão de entrega registrada obrigatoriamente na abertura. |

---