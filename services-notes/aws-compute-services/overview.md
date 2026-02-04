# ☁️ AWS Compute Services Overview

- Instâncias EC2s
- Containers (ECS,EKS)
- Serverless (Lambda, Fargate)

## Instâncias EC2s

- Rapidamente é possível construir e iniciar um novo servidor sem precisar adquirir um rack, cabos, memória, definir espaço fisíco, atualizar hardware e softwares, como em um servidor tradicional
- 4 noves de disponibilidade - 99,99%
- É possível escalar verticalmente de acordo com a necessidade, adicionando ou removendo recursos (memória, armazenamento, CPU)
- Instâncias otimizadas de acordo com o tipo de workload: memory optimized, compute optimized, storage optmized, accelerated computing, e general purpose (gp2, gp3)
- Diversos tipos de instâncias com diferentes opções de preços: On-demand, reserved instances, e spot instances
- EC2 dá controle completo para gerenciamento da instância

## Serverless

A nuvem já fornece uma camada de abstração que tira do cliente a resposabilidade de gerenciar a parte fisíca/hardware. Já com os serviços serverless, temos uma nova camada de abstração: o cliente apenas se procupa com o código da aplicação (as instâncias e o sistema operacional tbm fica abstraído).

- O cliente paga apenas pelo tempo de execução do serviço
- Aplicações “pequenas” que podem ser executadas em até 15 minutos
- Escalabilidade (aumento de recursos e instâncias) automática, totalmente gerenciado pelo AWS
- As funções lambdas são executadas em diferentes zonas de disponbilidade (redundância), minimizando a chance de down-time em caso de interrupção de uma AZ.
