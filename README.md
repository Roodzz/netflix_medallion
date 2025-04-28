# Projeto Netflix Catalog - Arquitetura Medallion

Este projeto utiliza dados do Kaggle sobre o catálogo da Netflix e explora os padrões da arquitetura Medallion para organizar e processar dados em camadas de bronze, prata e ouro. A arquitetura Medallion permite um fluxo de dados escalável e confiável, com a transformação dos dados em cada camada para análise e visualização mais eficazes.

## Objetivo

O objetivo deste projeto é demonstrar como implementar a arquitetura Medallion com dados reais do catálogo da Netflix, fornecendo insights sobre a organização e estruturação de dados para análises de alto desempenho.

## Estrutura da Arquitetura Medallion

A arquitetura Medallion é composta por três camadas principais:

1. **Camada Bronze**: Dados brutos, sem transformações.
2. **Camada Prata**: Dados limpos e transformados, com validação e algumas agregações.
3. **Camada Ouro**: Dados agregados e prontos para análise ou visualização, oferecendo insights mais profundos.

## Requisitos

Para rodar este projeto, você precisará das seguintes bibliotecas Python:

- `pandas`
- `pyarrow`
- `os`

Além disso, você precisará de uma conta no [Kaggle](https://www.kaggle.com) para acessar os dados do catálogo da Netflix.

## Como Rodar o Projeto

### 1. Clone o Repositório

Clone este repositório para o seu ambiente local:

```bash
git clone https://https://github.com/Roodzz/netflix_medallion.git
cd netflix_medallion
```

### 2. Crie um Ambiente Virtual

Recomenda-se criar um ambiente virtual para instalar as dependências isoladamente. No terminal, execute:

```bash
python -m venv venv
```

### 3. Ative o Ambiente Virtual

- No Windows:
  ```bash
  venv\Scripts\activate
  ```
- No macOS/Linux:
  ```bash
  source venv/bin/activate
  ```

### 4. Instale as Dependências

Instale as bibliotecas necessárias, utilizando o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 5. Acesse os Dados do Kaggle

Para baixar os dados do Kaggle, siga os seguintes passos:

- Crie uma conta no Kaggle e obtenha a chave API em [https://www.kaggle.com/docs/api](https://www.kaggle.com/docs/api).
- Após configurar a chave API, use o comando abaixo para baixar os dados do catálogo da Netflix:
  
  ```bash
  kaggle datasets download -d <dataset-name>
  ```

  Substitua `<dataset-name>` pelo nome do conjunto de dados que você deseja usar.

### 6. Execute o Projeto

Depois de configurar o ambiente, você pode executar os scripts para processar e analisar os dados, aplicando a arquitetura Medallion.

```bash
python process_data.py
```

### 7. Visualize os Resultados

Os resultados do processamento estarão disponíveis na camada "Ouro", onde você pode analisar e visualizar os insights extraídos dos dados do catálogo da Netflix.

## Contribuições

Contribuições são bem-vindas! Se você tem sugestões ou melhorias para o projeto, sinta-se à vontade para abrir um _pull request_.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).