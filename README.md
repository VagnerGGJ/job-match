# Analisador de PDF’s Assíncrono

---

Este é um projeto experimental voltado para estudos de microservices, processamento assíncrono com Kafka e análise de PDF’s usando Java.

O sistema simula um cenário onde empresas divulgam vagas de emprego com palavras-chave desejadas, e candidatos enviam currículos em PDF. Um serviço assíncrono processa esses currículos e calcula a compatibilidade com a vaga.

---

### Objetivos:

- Explorar arquitetura de microservices com Java.
- Processar currículos em PDF de forma assíncrona.
- Utilizar OCR com **Tess4J** para extrair texto de PDF’s escaneados.
- Aplicar mensageria com **Apache Kafka**.
- Implementar tratamento de falhas com **Dead Letter Queue (DLQ)**.

---

### Arquitetura: (Monorepo):

> job-match-pipeline/
>
>
> ├── services/                                         # Todos os microservices
>
> │   ├── recruitment-service/             # Futuro serviço REST API
>
> │   └── pdfprocessing-service/        # Kafka + OCR + análise
>
> ├── kafka/                                              # Tópicos, scripts e docs
>
> ├── shared/                                           # Modelos e utilitários comuns
>
> ├── storage/                                         # Pasta local para armazenar PDF’s
>
> ├── docker-compose.yml                 # Infra local
>
> └── README.md


---