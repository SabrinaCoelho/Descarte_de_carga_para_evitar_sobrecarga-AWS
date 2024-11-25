---
marp: true
---
# Descarte de carga para evitar sobrecarga AWS
###
###
### Alunos Sabrina Coelho e Matheus Rezende
### Prof. Roberto
---
## Definição e Conceito 
O descarte de carga é a prática de rejeitar seletivamente requisições quando um sistema está próximo de sobrecarregar, permitindo que ele mantenha a capacidade de atender às requisições mais críticas. Isso ajuda a evitar que o sistema se torne completamente inoperante devido a uma sobrecarga.
- Latência é p tempo que uma ação online leva para ser concluída, desde o envio da atividade até o seu destino. A latência é medida em milissegundos (ms).
- Throughput é o número total de solicitações por segundo que estão sendo enviadas ao servidor.
- Goodput é o subconjunto do throughput que é tratado sem erros e com latência baixa o suficiente para que o cliente faça uso da resposta.
- Lei de escalabilidade universal
- Lei de Amdahl
---
![Grafico](https://ibb.co/0CR4JFY)

O objetivo do descarte de carga é manter a latência baixa para as solicitações que o servidor decide aceitar, para que o serviço responda antes que o cliente atinja o tempo limite. Com essa abordagem, o servidor mantém alta disponibilidade para as solicitações que aceita e apenas a disponibilidade do tráfego em excesso é afetada.

---

## Funcionamento
Quando um sistema detecta que está atingindo seus limites de capacidade, ele começa a rejeitar requisições adicionais ou menos prioritárias. Essa abordagem permite que o sistema continue operando de forma eficiente, atendendo às requisições mais importantes e evitando falhas totais.

---

## Aplicabilidade e Casos de Uso
O descarte de carga é aplicável em sistemas que enfrentam picos de tráfego ou que dependem de recursos limitados. É especialmente útil em serviços web, APIs e sistemas distribuídos que precisam manter a disponibilidade mesmo sob alta demanda.

---

## Características
- **Detecção de Sobrecarga:** Monitoramento contínuo do sistema para identificar sinais de sobrecarga.
- **Priorização de Requisições:** Capacidade de identificar e priorizar requisições críticas.
- **Rejeição Seletiva:** Capacidade de rejeitar requisições menos importantes ou que consomem muitos recursos.

---

## Vantagens
- **Manutenção da Disponibilidade:** Permite que o sistema continue operando, mesmo sob alta demanda.
- **Prevenção de Falhas Totais:** Evita que o sistema se torne completamente inoperante devido à sobrecarga.
- **Eficiência de Recursos:** Garante que os recursos sejam utilizados de forma otimizada, atendendo às requisições mais importantes.

---

## Desvantagens e Limitações
- **Experiência do Usuário:** Usuários cujas requisições são rejeitadas podem ter uma experiência negativa.
- **Complexidade de Implementação:** Requer mecanismos sofisticados para detecção de sobrecarga e priorização de requisições.
- **Possível Perda de Dados:** Rejeitar requisições pode resultar na perda de informações ou operações não realizadas.

---

## Exemplos
- Elastic Load Balancing, que podem ser configuradas para implementar estratégias de descarte de carga.

---

## Outras Informações Importantes
O artigo enfatiza a importância de testar e monitorar continuamente os sistemas para garantir que as estratégias de descarte de carga sejam eficazes. Além disso, destaca que o descarte de carga deve ser parte de uma abordagem abrangente de gerenciamento de capacidade e resiliência do sistema.

---

# Agradecemos!
