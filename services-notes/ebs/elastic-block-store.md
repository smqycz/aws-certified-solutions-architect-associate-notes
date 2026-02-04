# 💿 Elastic Block Store (EBS)

Elastic Block Store (EBS) é um serviço de storage com foca em performance, já que este tipo de storage é o mais próximo da instância EC2, quando comparado com EFS e S3 (que são serviços regionais).

## Tipos de EBS

![EBS types](./ebs-types.png "EBS types")

### Provisioned IOPS - SSD

![Provisioned IOPS](./ebs-provisioned-iops.png "Provisioned IOPS")

### Provisioned IOPS - SSD

![Throughput Optimized - HDD](./ebs-throughput-optimized.png "Throughput Optimized - HDD")

> Apenas SSD podem ter EBS Multi Attach

### Cold HDD

![Cold HDD](./ebs-cold-hdd.png "Cold HDD")

### EBS - Magnetic

![EBS - Magnetic](./ebs-magnetic.png "EBS - Magnetic")