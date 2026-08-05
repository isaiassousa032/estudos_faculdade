# Backend - Sistema de Expedição Espacial

Este documento detalha a implementação do backend do Sistema de Gerenciamento de Expedição Espacial, desenvolvido utilizando Python e Flask. 

## Visão Geral

O backend atua como uma API RESTful, gerenciando a lógica central do simulador de missões espaciais. Ele recebe as requisições do frontend, processa os dados da expedição e os armazena de forma persistente. A aplicação utiliza o framework Flask para o roteamento e gerenciamento de requisições, e o SQLite como banco de dados relacional leve.

## Tecnologias e Bibliotecas

*   **Linguagem:** Python
*   **Framework Web:** Flask
*   **Manipulação de JSON:** `jsonify` (fornecido pelo Flask)
*   **Tratamento de Requisições:** `request` (fornecido pelo Flask)
*   **Banco de Dados:** SQLite (via módulo `sqlite3` nativo do Python)

## Estrutura de Dados e Modelagem

A entidade central do sistema é a **Missão**. A classe `Missao` foi implementada para representar e estruturar as informações de cada expedição.

### Entidade: `Missao`

Esta classe armazena todos os detalhes operacionais de uma missão.

*   **Atributos Principais:**
    *   `id`: Identificador único da missão (Inteiro).
    *   `nome_da_missao`: Nome oficial da expedição (String).
    *   `data_de_lancamento`: Data programada para a partida.
    *   `destino`: Local no espaço para onde a missão se dirige.
    *   `estado`: Fase atual do planejamento (ex: "Em planejamento", "Em execução").
    *   `tripulacao`: Lista contendo os nomes dos astronautas alocados.
    *   `duracao`: Tempo estimado de duração da missão.
    *   `status`: Status operacional geral (ex: "Ativo", "Cancelado").
    *   `carga_util`: Descrição dos equipamentos ou carga a bordo.

*   **Métodos:**
    *   `para_dicionario()`: Método utilitário crucial que serializa a instância da classe, convertendo todos os atributos em um dicionário Python. Este método é essencial para preparar os dados para o envio como resposta JSON pela API.

## Funcionalidades da API RESTful

A API foi desenhada para realizar operações CRUD (Create, Read, Update, Delete) sobre as missões. 

### Rota de Criação de Missões

O sistema expõe um endpoint para o registro de novas expedições espaciais.

*   **Endpoint:** `/missions`
*   **Método HTTP:** `POST`
*   **Fluxo de Execução:**
    1.  A função `create_mission` é acionada pela rota `@app.route('/missions', methods=['POST'])`.
    2.  Utilizando `request.get_json()`, o sistema extrai o payload enviado pelo frontend.
    3.  Uma nova instância da classe `Missao` é criada. Os dados recebidos (nome, data, destino, etc.) mapeiam diretamente os atributos do objeto. 
    4.  O sistema gerencia automaticamente a geração do `id` da missão através de uma variável de controle interna (`mission_id_control`), garantindo a unicidade de cada registro. A variável é incrementada após cada criação.
    5.  O objeto `Missao` recém-criado é adicionado à coleção de missões ativas (lista `missions`).
    6.  A API retorna uma resposta JSON contendo a mensagem "Nova missão criada com sucesso." e o respectivo código de status HTTP (201 Created).

*Nota: Em ambiente de desenvolvimento, a lista de missões é impressa no console para fins de depuração (`print(missions)`).*

## Configuração do Ambiente e Execução

### Pré-requisitos
*   Python 3.x instalado.

### Passos para rodar
1.  Crie e ative um ambiente virtual (recomendado):
    ```bash
    python -m venv venv
    # Windows: venv\Scripts\activate
    # Linux/Mac: source venv/bin/activate
    ```
2.  Instale as dependências:
    ```bash
    pip install Flask
    ```
3.  Inicie o servidor Flask:
    ```bash
    python app.py
    ```
    O servidor estará disponível por padrão na porta 5000 (ex: `http://localhost:5000`).
