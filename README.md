# Wisdom Core

**Wisdom Core** é uma solução de Data LakeHouse projetada para gerenciar, processar e armazenar grandes volumes de dados de maneira eficiente, especialmente em ambientes com recursos limitados. Ele atua como o destino principal dos dados coletados pelo **Wisdom Reach**, unificando armazenamento e processamento para análises rápidas e confiáveis. Sua arquitetura leve e escalável é otimizada para clusters arm64, proporcionando flexibilidade e desempenho para aplicações modernas.

## 🚀 Funcionalidades

- **Armazenamento de Dados**: Organização e armazenamento de dados em formatos estruturados e não estruturados.
- **Processamento em Lote e Streaming**: Suporte a pipelines ETL para transformar e enriquecer dados.
- **Conectividade**: Integração com Apache Kafka para ingestão de dados em tempo real.
- **Consultas Avançadas**: Consultas rápidas e escaláveis para análise de grandes volumes de dados.

## 🛠️ Tecnologias Utilizadas

- **Apache Spark**: Processamento de dados em lote e streaming.
- **Apache Kafka**: Sistema de mensageria para ingestão de dados em tempo real.
- **Delta Lake**: Armazenamento otimizado para um Data LakeHouse.
- **Docker**: Empacotamento e deploy em contêineres.
- **k3s**: Orquestração para clusters leves.

## 📦 Estrutura do Repositório

```
wisdom-core/
├── ingestion/            # Módulos para ingestão de dados
├── processing/           # Pipelines de processamento e transformação
├── storage/              # Configurações e scripts para armazenamento
├── configs/              # Configurações gerais
├── docker/               # Arquivos Docker para deploy
├── tests/                # Testes unitários e de integração
└── README.md             # Documentação do projeto
```

## 🌐 Pré-requisitos

1. **Docker** e **Docker Compose** instalados.
2. (Opcional) Um cluster **k3s** para deploy em ambiente distribuído.

## 🛠️ Configuração

1. Clone o repositório:
   ```bash
   git clone https://github.com/santanaMd/wisdom-core.git
   cd wisdom-core
   ```

2. Configure os arquivos em `configs/` conforme sua infraestrutura.

3. Construa os contêineres:
   ```bash
   docker-compose build
   ```

4. Inicie os serviços:
   ```bash
   docker-compose up -d --env $ENV_FILE
   ```

## 🧪 Testes

Execute os testes unitários para validar o funcionamento dos módulos:

```bash
pytest tests/
```

## 📖 Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do repositório.
2. Crie uma branch para sua feature ou correção de bug:
   ```bash
   git checkout -b minha-feature
   ```
3. Commit suas alterações:
   ```bash
   git commit -m "Descrição da minha feature"
   ```
4. Envie as alterações:
   ```bash
   git push origin minha-feature
   ```
5. Abra um pull request.

## 📝 Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

---

Este projeto faz parte do ecossistema Wisdom, que inclui o [Wisdom Reach](https://github.com/santanaMd/wisdom-reach).
