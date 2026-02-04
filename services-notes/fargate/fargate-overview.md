# AWS Fargate

O AWS Fargate é um serviço serverless que gerencia a orquestração de containers, sem a necessidade do cliente lidar com a parte de provisionamento, configuração e escalonamento de máquinas virtuais para executar containers.  

💡 **A arquitetura do AWS Fargate fornece um ambiente de computação sem servidor para executar contêineres sem gerenciar a infraestrutura subjacente.**

## Use Cases

**Microservices architecture implementation (Implementação de arquitetura de microsserviços):** com o AWS Fargate é possível focar apenas no desenvolvimento do código dos microserviços, sem se preocupar com a complexidade da infraestrutura. O modelo de isolamento do AWS Fargate está perfeitamente alinhado com os princípios dos microserviços - cada serviço deve ser independente e autocontido. 

**Batch processing workloads (carge de processamento em lote):** Fargate consegue rapidamente provisionar os recursos de infra para executar cada lote de processamento e automaticamente liberá-los quando o processo é completado. Assim, não mantém recursos oceosos, além da economia financeira. 

**CI/CD pipeline automation**: uso  do AWS Fargate para entrega contínua, como compilação, execução de testes automatizados e implantação de tarefas. Isso elimina a necessidade de gerenciar servidores e também reduz tempo oceoso que pode ocorrer entre commits de código. 

**Web applications and APIs (aplicações web e APIs):** O Fargate automática escalona a aplicação para atender o tráfico (aumento/diminui recursos de acordo com a necessidade), enquanto mantém as aplicações isoladas.
