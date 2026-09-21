# ChargeVolt
## Challenge GoodWe 2026 - Turma 1CCPY
### Integrantes:
* Gabriela Caetano - RM: 572738
* Laura Pícari - RM: 569914
* Lucas Neves - RM: 572679
* João Victor - RM: 571630
* Beatriz Araújo - RM: 570619


## 1. O Problema
Ausência de mecanismos inteligentes em muitos eletropostos comerciais para gerenciar sessões de recarga, controlar o consumo energético e automatizar processos de cobrança e pagamento. Com o crescimento da mobilidade elétrica, essa limitação pode gerar desperdício de energia, sobrecarga da rede elétrica e pouca flexibilidade para os usuários.

## 2. Nossa Proposta
O ChargeVolt é um sistema inteligente para eletropostos que permite ao usuário gerenciar sua recarga de forma prática e personalizada. O sistema conta com um aplicativo mobile (Frontend) e um motor de simulação em Python. 

## 3. Arquitetura do Sistema e Integração
A solução é dividida em duas camadas principais que se comunicam:
1. **Frontend (Aplicativo Mobile):** Desenvolvido via Thunkable. Responsável pela interface do usuário, cadastro, seleção de estações, pagamento, agendamento e visualização do histórico (aplicativo apenas de simulação).
2. **Backend (Simulador Python):** Responsável pela lógica de negócios, cálculo de energia (kWh), precificação (R$ 0,90/kWh), simulação do sensor do carregador (Hardware) e Dashboard Administrativo.

### Diagrama de Blocos
```mermaid
graph TD
    A[Usuário] -->|Interage| B(App Mobile - React Native)
    B -->|Envia Dados| C{Backend / Simulador Python}
    C -->|Processa Pagamento| D[Divisão de Receita: 90% Local / 10% GoodWe]
    C -->|Simula Hardware| E[Sensor do Eletroposto]
    E -->|Retorna Dados| C
    C -->|Atualiza Status| B
    B -->|Exibe| F[Dashboard Admin & Histórico]
