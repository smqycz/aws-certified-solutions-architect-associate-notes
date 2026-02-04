# Practice exame #1

1. O Cost Explorer está mostrando cobranças maiores do que o esperado para volumes do Amazon Elastic Block Store (Amazon EBS) conectados a servidores de aplicativos em uma conta de produção. Uma parte significativa das cobranças do Amazon EBS refere-se a volumes que foram criados como tipos de volume SSD de IOPS provisionado (io2). O controle de custos é a maior prioridade para essa aplicação. Quais etapas o usuário deve realizar para analisar e reduzir os custos do EBS sem experimentar nenhum tempo de inatividade do aplicativo? (Selecione DUAS.)

  - A. Usar a ação ModifyInstanceAttribute do Amazon EC2 para habilitar a otimização do EBS nas instâncias do servidor do aplicativo.

  - B. Usar a ação GetMetricData do Amazon CloudWatch para avaliar as operações e os bytes de leitura/gravação de cada volume.

  - C. Usar a ação ModifyVolume do Amazon EC2 para reduzir o tamanho dos volumes io2 subutilizados.

  - D. Usar a ação ModifyVolume do Amazon EC2 para alterar o tipo de volume dos io2 subutilizados para SSD de uso geral (gp3).

  - E. Usar a ação PutBucketPolicy do Amazon S3 para migrar snapshots de volumes existentes para o Amazon S3 Glacier Flexible Retrieval.

  <details markdown=1>
    <summary markdown='span'>Resposta</summary>
    Resposta correta: B & D
  </details>

---

2. 1. Uma empresa está usando conexões do AWS Site-to-Site VPN para conectividade segura com os recursos da Nuvem AWS em locais no local. Devido a um aumento no tráfego entre as conexões VPN para as instâncias do Amazon EC2, os usuários estão enfrentando uma conectividade VPN mais lenta. A equipe de rede informa que a conexão com a Internet usada para a VPN tem uma taxa de transferência adicional não utilizada. Qual solução melhorará a taxa de transferência da VPN?

  - A. Implementar vários gateways do cliente na mesma rede.
  - B. Configurar um gateway privado virtual com roteamento de vários caminhos de custo igual e vários canais.
  - C. Usar um transit gateway com roteamento de vários caminhos de custo igual e adicionar outros túneis VPN
  - D. Aumentar o número de túneis na configuração da VPN.

  <details markdown=1>
    <summary markdown='span'>Resposta</summary>
    Resposta correta: C
    <p>Cada conexão de AWS Site-to-Site VPN tem 2 túneis, portanto, não é possível configurar outros túneis. Limite de banda da conexão AWS Site-to-Site: 1.25 Gpbs. Com o roteamento ECMP (roteamento de vários caminhos de custo igual), é possível agregar várias conexões VPN para obter uma taxa de transferência efetiva mais alta.</p>
  </details>

---

3. Uma empresa quer criar uma aplicação que transmitirá informações de saúde protegidas (PHI) para milhares de consumidores de serviços em diferentes contas da AWS. Os servidores da aplicação ficarão em sub-redes privadas da VPC. O roteamento da aplicação deve ser tolerante a falhas. O que deve ser feito para atender a esses requisitos?

  - A. Criar um serviço de endpoint da VPC e conceder permissões aos consumidores de serviços específicos para criar uma conexão.

  - B. Criar uma conexão de gateway privado virtual entre cada par de VPCs do provedor de serviços e VPCs do consumidor de serviços.

  - C. Criar um Application Load Balancer interno na VPC do provedor de serviços e colocar os servidores da aplicação por trás dele.

  - D. Criar um servidor de proxy na VPC do provedor de serviços para encaminhar solicitações de consumidores de serviços para os servidores da aplicação.

<details markdown=1>
  <summary markdown="span">Resposta</summary> Resposta correta: A 
  <p>Com o VPC Endpoint, o tráfego não sai para a internet, ficando totalmente privado. Um gateway privado virtual fornece acesso da AWS à internet.</p> </details>

---

4. Uma equipe de desenvolvimento está implantando um novo produto na AWS e usando o AWS Lambda como parte da implantação. A equipe aloca 512 MB de memória para uma das funções do Lambda. Com essa alocação de memória, a função é concluída em dois minutos. A função é executada milhões de vezes mensalmente, e a equipe de desenvolvimento está preocupada com o custo. A equipe realiza testes para ver como diferentes alocações de memória do Lambda afetam o custo da função. Quais etapas reduzirão os custos do Lambda para o produto? (Selecione DUAS respostas.)

  - A. Aumentar a alocação de memória dessa função do Lambda para 1.024 MB se essa alteração reduzir o tempo de execução de cada função para menos de um minuto.

  - B. Aumentar a alocação de memória dessa função do Lambda para 1.024 MB se essa alteração reduzir o tempo de execução de cada função para menos de noventa segundos.

  - C. Diminuir a alocação de memória dessa função do Lambda para 256 MB se essa alteração reduzir o tempo de execução de cada função para menos de quatro minutos.

  - D. Aumentar a alocação de memória dessa função do Lambda para 2.048 MB se essa alteração reduzir o tempo de execução de cada função para menos de um minuto.

  - E. Diminuir a alocação de memória dessa função do Lambda para 256 MB se essa alteração reduzir o tempo de execução de cada função para menos de cinco minutos.

  <details markdown=1>
    <summary markdown="span">Resposta</summary> Respostas corretas: A e C
    <p>Cálculo de custo: ao dobrar a memória, o tempo de execução deve cair aproximadamente pela metade para manter ou reduzir o custo. Ao aumentar para 2.048 MB (quatro vezes mais memória), o tempo precisaria cair proporcionalmente (para menos de 30 segundos), o que não ocorre no cenário descrito.</p>
  </details>

---

5. Uma empresa quer construir uma infraestrutura imutável para seus aplicativos de software. A empresa quer testar os aplicativos antes de enviar tráfego para eles e busca uma solução eficiente que limite os efeitos de bugs. Qual combinação de etapas um solutions architect deve recomendar? (Selecione DUAS.)

  - A. Usar o AWS CloudFormation para atualizar a infraestrutura de produção e reverter a pilha se a atualização falhar.

  - B. Aplicar o roteamento ponderado do Amazon Route 53 para testar o ambiente de teste e aumentar gradualmente o tráfego à medida que os testes passam.

  - C. Aplicar o roteamento de failover do Amazon Route 53 para testar o ambiente de teste e fazer failover para o ambiente de produção se os testes forem aprovados.

  - D. Usar o AWS CloudFormation com um parâmetro definido para o valor de preparação em um ambiente separado que não seja o ambiente de produção.

  - E. Usar o AWS CloudFormation para implantar o ambiente de teste com uma política de exclusão de snapshot e reutilizar os recursos no ambiente de produção se os testes forem aprovados.

  <details markdown=1>
    <summary markdown="span">Resposta</summary>
    Respostas corretas: B e D 
    <p>Atualizar diretamente os recursos de produção pode impactar usuários finais. A abordagem correta é utilizar um ambiente separado para testes e controlar gradualmente o tráfego usando roteamento ponderado.</p>
  </details>

---

6. Um ambiente tem um grupo do Auto Scaling em duas zonas de disponibilidade chamadas AZ-A e AZ-B. A AZ-A tem quatro instâncias do Amazon EC2 e a AZ-B tem três. O grupo usa a política de terminação padrão e nenhuma instância está protegida contra scale-in. O que acontece durante um evento de redução de escala?

  - A. O Auto Scaling escolherá uma instância aleatoriamente.

  - B. O Auto Scaling terminará a instância com a configuração de lançamento mais antiga.

  - C. O Auto Scaling selecionará a zona de disponibilidade com quatro instâncias do EC2 e continuará a avaliação.

  - D. O Auto Scaling terminará a instância com a nova hora de faturamento mais próxima.

  <details markdown=1>
    <summary markdown="span">Resposta</summary> 
    Resposta correta: C 
    <p>Como o número de instâncias está desbalanceado entre as zonas de disponibilidade, o Auto Scaling primeiro seleciona a zona com mais instâncias para restaurar o equilíbrio.
    </p>
  </details>

---
7. Um arquiteto de soluções está projetando uma solução de banco de dados que deve suportar alta taxa de leitura e gravação aleatórias de disco, fornecer performance consistente e garantir persistência de longo prazo. Qual solução atende a esses requisitos?

  - A. Um volume de IOPS provisionadas do Amazon Elastic Block Store (Amazon EBS)

  - B. Um volume de uso geral do Amazon Elastic Block Store (Amazon EBS)

  - C. Um volume magnético do Amazon Elastic Block Store (Amazon EBS)

  - D. Um armazenamento de instância do Amazon EC2

  <details markdown=1>
    <summary markdown="span">Resposta</summary>
    Resposta correta: A 
    <p>Volumes com IOPS provisionadas oferecem performance consistente e são ideais para cargas de trabalho com alta taxa de leitura e gravação aleatórias. Volumes de uso geral não garantem essa consistência.</p>
  </details>

---

8. Um solutions architect está projetando uma arquitetura altamente disponível com Application Load Balancer, Auto Scaling e um banco de dados Amazon RDS Multi-AZ. É necessário um plano de recuperação multirregional com RTO de 30 minutos, sem replicar toda a arquitetura e usando a região secundária apenas se necessário. Qual estratégia atende aos requisitos?

  - A. Backup e restauração

  - B. Multissite ativo/ativo

  - C. Luz piloto

  - D. Standby passivo

  <details markdown=1>
    <summary markdown="span">Resposta</summary> 
    Resposta correta: C 
    <p>O modelo de Luz Piloto (Pilot light) replica apenas os componentes essenciais, reduzindo custos e permitindo recuperação rápida. Standby passivo (Warm standby) replica toda a infraestrutura, o que não atende às restrições orçamentárias.</p>
  </details>

---
9. Uma empresa usa o Amazon DynamoDB com taxa de transferência provisionada para o inventário de um site de e-commerce. Durante ofertas relâmpago, o banco não suporta o pico de transações, mas funciona bem em períodos normais. Qual solução resolve o problema de performance?

  - A. Alternar o DynamoDB para o modo sob demanda durante as ofertas relâmpago.

  - B. Implementar o DynamoDB Accelerator (DAX).

  - C. Usar o Amazon Kinesis para enfileirar as transações.

  - D. Usar o Amazon Simple Queue Service (Amazon SQS) para enfileirar as transações no DynamoDB.

  <details markdown=1>
    <summary markdown="span">Resposta</summary>
    Resposta correta: A 
    <p>O modo sob demanda permite que o DynamoDB escale automaticamente para lidar com picos repentinos de tráfego, como em ofertas relâmpago.</p>
  </details>

---

10. Um arquiteto de soluções está projetando uma aplicação híbrida com AWS Direct Connect (DX). A conectividade entre o datacenter on-premises e a AWS deve ser altamente resiliente. Qual configuração atende a esse requisito?

  - A. Configurar uma conexão do DX com uma VPN sobre ela.

  - B. Configurar uma conexão do DX usando o parceiro mais confiável.

  - C. Configurar várias interfaces virtuais sobre uma única conexão do DX.

  - D. Configurar conexões do DX em vários locais do DX.

  <details markdown=1>
    <summary markdown="span">Resposta</summary>
    Resposta correta: D 
    <p>Utilizar múltiplas conexões do Direct Connect em locais diferentes aumenta a resiliência. Usar o mesmo DX não protege contra falhas físicas ou de local.</p>
  </details>

---
11. 1. Um usuário está projetando um novo serviço que recebe atualizações de localização de 3.600 carros alugados a cada hora. Os carros fazem upload de sua localização em um bucket do Amazon S3. Cada localização deve ser verificada com relação à distância do local de locação original. Quais serviços vão processar as atualizações e escalar automaticamente?

  - A. Amazon EC2 e Amazon Elastic Block Store (Amazon EBS)

  - B. mazon Kinesis Data Firehose e Amazon S3

  - C. Amazon Elastic Container Service (Amazon ECS) e Amazon RDS

  - D. Eventos do Amazon S3 e AWS Lambda

  <details markdown=1>
    <summary markdown="span">Resposta</summary>
    Resposta correta: D 
    <p>Antes de salvar no bucket, precisa fazer a verificação. A única solução que permite isso é o Amazon S3 + Lambda. </p>
  </details>

---
12. 1. Uma empresa quer medir a eficácia das campanhas de marketing recentes. A empresa executa o processamento em batch em arquivos .csv de dados de vendas e armazena os resultados em um bucket do Amazon S3 uma vez a cada hora. O bucket do S3 contém petabytes de objetos. A empresa executa consultas únicas no Amazon Athena para determinar quais produtos são mais populares em uma data específica para uma região específica. Às vezes, as consultas falham ou demoram mais do que o esperado para concluir a execução. Quais ações um solutions architect deve tomar para melhorar o desempenho e a confiabilidade da consulta? (Selecione DUAS.)
    - A. Reduzir os tamanhos dos objetos do S3 para menos de 128 MB.
    - B. Seperar os dados por data e região no Amazon S3.
    - C. Armazenar os arquivos como objetos grandes e únicos no Amazon S3.
    - D. Usar o Amazon Kinesis Data Analytics para executar as consultas como parte da operação de processamento em batch.
    - E. Usar um processo de extração, transformação e carregamento (ETL) do AWS Glue para converter os arquivos .csv no formato Apache Parquet.

  <details markdown=1>
    <summary markdown="span">Resposta</summary>
    Respostas corretas: B e E

    O problema quer melhorar a performance da consulta SQL utilizando o Athena. O Kinesis Data Analytics é uma ferramenta que transforma e analisa dados de streaming em tempo real. Você não pode usar essa ferramenta para consultar dados específicos.
  </details>