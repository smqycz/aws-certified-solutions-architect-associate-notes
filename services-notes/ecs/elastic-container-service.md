# 📦 Elastic Container Service (ECS)

ECS é um serviço totalmente gerenciado de orchestração de containers que ajuda no processo de implantar, gerenciar e escalar aplicações containerizadas. Ele elimina a necessidade de operar seu próprio software de orquestração de contêineres, dimensionar um cluster de máquinas virtuais ou agendar contêineres nessas máquinas virtuais.

O Amazon ECS lida com as tarefas complexas de alocação de contêineres com base nos seus requisitos de recursos e necessidades de disponibilidade. Ele também mantém a disponibilidade dos aplicativos e ajuda você a aumentar ou diminuir a escala dos seus aplicativos em contêineres.

## Funcionalidades core

O ECS é uma plataforma robusta de gerenciamento de containers. O ECS gerencia toda a infraestrutura de hardware necessário para exxecutar os container em escala, além de lidar automaticamente com tarefas de posicionamento de containers, monitoramente e recuperação de falhas.

- **Orquestração de containers**
    - É a funcionalidade principal, onde são especificados os recursos necessários, como CPU, memória, configuração de rede, dependências entre containers, através de definições de tarefas (task). Além disso, lida automaticamente com tarefas de posicionamento de containers, monitoramente e recuperação de falhas.
- **Gerenciamento de clusters**
    - É a organização dos recursos computacionais em grupos lógicos chamados de clusters
- **Gerenciamento do ciclo de vida da aplicação**
    - Gerencia todo o ciclo de vida da aplicação, incluindo implantação, dimensionamento, atualizações, e a finalização de containers.

## Conceitos técnicos

- **Containers**: pacotes executáveis, leves e autônomos que possui tudo o que precisa para executar o software. Contém o código da aplicação, configurações, bibliotecas, etc.
- **Task definition:** definição de 1 ou mais containers
- **Tasks:** instanciação de uma definição de tarefa dentro de um cluster do Amazon ECS
    - Services
    - Clusters
    - Launch types
    - Container agent
    - Capacity providers
    - Task placement strategies