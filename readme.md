# Jupyter Notebook com Docker Compose

Este projeto fornece um ambiente de desenvolvimento para Python 3 utilizando Jupyter Notebook, configurado via Docker Compose. O Jupyter Notebook é executado em um container Docker, facilitando a criação e execução de notebooks de forma isolada e consistente.

## Pré-requisitos

- [Docker](https://www.docker.com/get-started) instalado
- [Docker Compose](https://docs.docker.com/compose/install/) instalado

## Como Usar

### 1. Clone este repositório

```bash
git clone https://github.com/seu-usuario/jupyter-docker-compose.git
cd jupyter-docker-compose
```

### 2. Inicie o container
Execute o seguinte comando para iniciar o Jupyter Notebook:
```bash
docker-compose up
```

### 3. Acesse o Jupyter Notebook
Após iniciar o container, acesse o Jupyter Notebook no seu navegador em http://localhost:8888.

### 4. Trabalhe nos seus notebooks
Os notebooks são armazenados na pasta ./notebooks do seu diretório local e estão sincronizados com o container Docker. Qualquer alteração feita nos notebooks será preservada no seu sistema de arquivos local.

- Parando o Container
Para parar o container, pressione Ctrl+C no terminal onde o Docker Compose está rodando, ou execute:
```bash
docker-compose down
```

### 5. Customização
Se precisar instalar pacotes Python adicionais, você pode:

Adicionar os comandos de instalação ao arquivo Dockerfile (se você criar um), ou
Executar !pip install <pacote> diretamente em uma célula do Jupyter Notebook.

### Pasta NOTEBOOKS - Volume com persistência 
Nao esqueça de dar a permissao adequada para pasta que salvará os notebooks
```
mkdir notebooks
chmod -R 777 ./notebooks
```


