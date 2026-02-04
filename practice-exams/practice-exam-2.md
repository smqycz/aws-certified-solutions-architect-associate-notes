## Practice Exam #2

1. Uma empresa está migrando suas cargas de trabalho para a AWS. A empresa possui dados sensíveis e críticos em bancos de dados relacionais on-premises executados em instâncias do SQL Server. A empresa deseja usar soluções de nuvem da AWS para aumentar a segurança e reduzir a sobrecarga operacional para os bancos de dados. Qual solução atenderá a esses requisitos?

  - A. Migrar os bancos de dados para o Amazon EC2. Usar uma chave gerenciada pelo AWS Key Management Service (AWS KMS) para criptografia.

  - B. Migrar os bancos de dados para uma instância Amazon RDS para SQL Server com configuração Multi-AZ. Usar uma chave gerenciada pelo AWS Key Management Service (AWS KMS) para criptografia.

  - C. Migrar os dados para o Amazon S3. Usar o Amazon Macie para segurança e proteção de dados.

  - D. Migrar os bancos de dados para o Amazon DynamoDB. Usar o Amazon CloudWatch Logs para garantir a segurança dos dados.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: B </details>

---
2. Uma empresa tem uma aplicação em que os clientes fazem upload de imagens para um bucket Amazon S3. Atualmente, as imagens são processadas à noite por uma Amazon EC2 Spot Fleet. O processamento de cada imagem leva 2 minutos e requer 512 MB de memória. O arquiteto precisa processar as imagens assim que forem enviadas. Qual alteração atende ao requisito da forma mais econômica?

  - A. Usar S3 Event Notifications para escrever mensagens em uma fila do Amazon SQS e processar com AWS Lambda.

  - B. Usar S3 Event Notifications para escrever mensagens em uma fila do Amazon SQS e processar com uma EC2 Reserved Instance.

  - C. Usar S3 Event Notifications para publicar mensagens em um tópico do Amazon SNS e processar com um contêiner no Amazon ECS.

  - D. Usar S3 Event Notifications para publicar mensagens em um tópico do Amazon SNS e processar com AWS Elastic Beanstalk.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: A 
<blockquote>O AWS Lambda pode executar por até 15 minutos e suporta até 10 GB de memória, sendo uma opção econômica e adequada para processamento sob demanda.</blockquote> </details>

----

3. Um arquiteto de soluções precisa revisar buckets do Amazon S3 para descobrir informações pessoalmente identificáveis (PII) armazenadas nas regiões us-east-1 e us-west-2. Qual solução atende ao requisito com o MENOR esforço operacional?

  - A. Configurar o Amazon Macie em cada região e criar jobs para analisar os dados no S3.

  - B. Configurar o AWS Security Hub e criar regras do AWS Config para analisar dados no S3.

  - C. Configurar o Amazon Inspector para analisar os dados no S3.

  - D. Configurar o Amazon GuardDuty para analisar os dados no S3.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: A <blockquote>O AWS Security Hub atua como um serviço centralizador, mas quem identifica e classifica dados sensíveis no S3 é o Amazon Macie.</blockquote> </details>

---
4. Recentemente, todos os snapshots do EBS da empresa foram acidentalmente excluídos ao executar um script de limpeza de snapshots que remove todos os snapshots expirados do EBS. Um arquiteto de soluções precisa atualizar a arquitetura para evitar perda de dados sem reter os snapshots do EBS indefinidamente. Qual solução atenderá a esses requisitos com o menor esforço de desenvolvimento?

  - A. Alterar a política do IAM para negar exclusão de snapshots.

  - B. Copiar os snapshots do EBS para outra região da AWS após completar os snapshots diariamente.

  - C. Criar uma regra de retenção de snapshots do EBS de 7 dias no Recycle Bin e aplicar a regra a todos os snapshots.

  - D. Copiar os snapshots do EBS para o Amazon S3 Standard-Infrequent Access (S3 Standard-IA).

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: C </details>

---
5. Uma empresa usa o Amazon RDS para PostgreSQL na região us-east-1. Relatórios quase em tempo real usando ML causam degradação de desempenho durante o horário comercial. O que deve ser feito para melhorar o desempenho?

  - A. Criar uma réplica de leitura em outra região e gerar relatórios a partir dela.

  - B. Ativar Multi-AZ e gerar relatórios a partir do banco standby.

  - C. Usar AWS DMS para replicar os dados para outro banco.

  - D. Criar uma réplica de leitura na região us-east-1 e gerar relatórios a partir dela.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: D <blockquote>Réplica de leitura em outra região aumenta custo e latência. A réplica na mesma região reduz impacto no banco primário sem penalidades de latência.</blockquote> </details>

---
6. Uma empresa deseja analisar erros de “Acesso negado” e “Não autorizado” relacionados ao IAM. O AWS CloudTrail está ativado. Qual solução exige o menor esforço?

  - A. Usar AWS Glue com scripts personalizados.

  - B. Usar AWS Batch com scripts personalizados.

  - C. Consultar logs do CloudTrail usando Amazon Athena.

  - D. Usar Amazon QuickSight para criar dashboards.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: C </details>

---
7. Uma aplicação web pública em EC2 e RDS terá aumento de tráfego durante um feriado. O arquiteto precisa analisar o desempenho com granularidade máxima de 2 minutos. O que deve ser feito?

  - A. Enviar logs para o Amazon Redshift e analisar com QuickSight.

  - B. Habilitar monitoramento detalhado nas instâncias EC2 e usar métricas do CloudWatch.

  - C. Criar funções Lambda para buscar logs no CloudWatch Logs.

  - D. Enviar logs para o Amazon S3 e processar com Redshift.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: B <blockquote>O monitoramento padrão do EC2 coleta métricas a cada 5 minutos. O monitoramento detalhado reduz o intervalo para 1 minuto.</blockquote> </details>

---
8. Um aplicativo de envio de documentos usa Amazon S3. A solução deve evitar exclusão acidental e manter todas as versões dos documentos disponíveis. Usuários devem poder modificar os arquivos. Quais ações devem ser tomadas? (Selecione DUAS)

  - A. Ativar versionamento no bucket.

  - B. Definir permissões somente leitura.

  - C. Ativar exclusão com MFA no bucket.

  - D. Anexar uma política IAM ao bucket.

  - E. Criptografar o bucket com SSE-S3.

<details markdown=1> <summary markdown="span">Resposta</summary> Respostas corretas: A e C <p></p> </details>


---
9. Uma empresa deseja reduzir custos de backup eliminando fitas físicas, mantendo compatibilidade com fluxos de backup existentes. O que deve ser recomendado?

  - A. Conectar aplicativos ao AWS Storage Gateway via NFS.

  - B. Conectar aplicativos ao AWS Storage Gateway usando uma biblioteca de fitas virtuais iSCSI (VTL).

  - C. Criar um sistema de arquivos Amazon EFS via NFS.

  - D. Criar um sistema de arquivos Amazon EFS via iSCSI.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: B <p></p> </details>

---
10. Uma aplicação web usa múltiplas instâncias EC2 Linux e volumes EBS. A empresa deseja aumentar a resiliência em caso de falhas. O que deve ser feito?

  - A. Criar ALB com Auto Scaling e usar S3 One Zone-IA.

  - B. Criar ALB com Auto Scaling e usar instance store.

  - C. Executar EC2 em cada AZ com volumes EBS anexados.

  - D. Criar ALB com Auto Scaling em várias AZs e armazenar dados no Amazon EFS.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: D <blockquote>Instance store é volátil. O Amazon EFS permite armazenamento compartilhado e persistente entre várias instâncias EC2.</blockquote> </details>

---
11. Uma plataforma financeira usa contêineres Docker em microsserviços. É necessário acesso ao sistema operacional das instâncias que executam os contêineres. Qual opção deve ser escolhida?

  - A. EKS com infraestrutura gerenciada do Kubernetes.

  - B. ECS com tipo de inicialização EC2.

  - C. ECS com tipo de inicialização Fargate.

  - D. AWS Lambda usando imagem de contêiner.

<details markdown=1> <summary markdown="span">Resposta</summary> Resposta correta: B <p></p> </details>

---
12. Um arquiteto criou uma nova sub-rede em uma VPC e lançou uma instância EC2, mas não consegue acessá-la pela internet. Quais ações devem ser realizadas? (Selecione DUAS)

  - A. Verificar se o Security Group permite tráfego de saída.

  - B. Verificar se a instância possui um endereço IP público.

  - C. Verificar se há um Gateway NAT configurado.

  - D. Verificar se a tabela de rotas da sub-rede tem uma rota para um Gateway de Internet.

  - E. Verificar se é possível pingar a instância de outra sub-rede.

<details markdown=1> <summary markdown="span">Resposta</summary> Respostas corretas: B e D <blockquote>O acesso é de entrada, não de saída. Security Group é statefull. Gateway NAT é usado para que instâncias EC2s em sub-redes privadas possam acessar a internet. O essencial é a instância EC2 ter um IP público e rota para o Internet Gateway.</blockquote> </details>