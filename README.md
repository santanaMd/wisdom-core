# Wisdom Core

**Wisdom Core** é o núcleo de dados do ecossistema Wisdom, projetado para ingestão, armazenamento e processamento escalável de dados dinâmicos coletados por agentes no projeto [Wisdom Reach](https://github.com/santanaMd/wisdom-reach). Este Data Lakehouse combina a flexibilidade de um Data Lake com a estrutura analítica de um Data Warehouse, possibilitando análises avançadas e insights estratégicos.

---

## **Principais Funcionalidades**
- **Ingestão via Kafka**: Dados de múltiplas fontes são integrados através de tópicos configuráveis no Kafka.
- **Armazenamento Escalável**: Dados brutos e processados organizados em camadas (bronze, silver, gold) no formato Parquet.
- **Processamento Distribuído**: Apache Spark para transformações robustas em tempo real e batch.
- **Alta Compatibilidade**: Arquitetura otimizada para rodar em Kubernetes (K3s) com suporte a ARM64.
- **Análises Rápidas**: Integração com Trino para consultas SQL diretas sobre o Data Lakehouse.

---

## **Arquitetura**
1. **Kafka (Ingestão)**:
   - Pontos de entrada dos dados provenientes dos agentes do Wisdom Reach.
   - Tópicos configurados para diferentes tipos de dados, garantindo separação e organização.
2. **Camadas do Data Lakehouse**:
   - **Bronze**: Dados brutos, armazenados como recebidos.
   - **Silver**: Dados transformados e validados.
   - **Gold**: Dados otimizados e agregados para análise.
3. **Processamento**:
   - Apache Spark realiza transformações e organiza os dados nas camadas do Lakehouse.
4. **Consulta**:
   - Trino permite executar consultas SQL em toda a estrutura.
5. **Armazenamento**:
   - MinIO (compatível com S3) para armazenamento distribuído e eficiente.

---

## **Requisitos**
- Cluster Kubernetes (K3s)
- Docker configurado com suporte a ARM64
- Apache Kafka para ingestão
- Ferramentas de CLI:
  - `kubectl`
  - `helm`

---

## **Instalação**
### Passos Rápidos
1. Clone o repositório:
   ```bash
   git clone https://github.com/santanaMd/wisdom-core.git
