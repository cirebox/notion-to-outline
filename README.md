# notion-to-outline

A ferramenta que extrai páginas e blocos do Notion e gera um esboço hierárquico. Este projeto permite exportar a estrutura do seu espaço de trabalho no Notion para um formato de outline, facilitando a visualização, compartilhamento ou reutilização dos dados do Notion. A aplicação interage com a API do Notion para recuperar os títulos das páginas e seu conteúdo associado, transformando-os em um formato de outline estruturado.

## Funcionalidades

- **Autenticação com a API do Notion**: A aplicação usa um token de integração para acessar dados no Notion.
- **Extração de páginas do Notion**: Busca e extrai informações de páginas dentro de um banco de dados do Notion.
- **Geração de Outline**: Converte os dados extraídos em um formato hierárquico de outline.
- **Extração de blocos e subtítulos**: Faz a extração de blocos e subtítulos dentro das páginas, criando uma estrutura de dados bem organizada.

## Requisitos

Antes de rodar a aplicação, verifique se você tem o seguinte:

- **Python 3.x**: A aplicação foi desenvolvida para Python 3.
- **Bibliotecas**:
    - `requests` para fazer requisições HTTP à API do Notion.
    - Você pode instalar essas dependências utilizando o comando:
      ```bash
      pip install requests
      ```

- **Token de Integração do Notion**:
    - Você precisa de um token de autenticação da API do Notion, que pode ser gerado no [Notion Developers](https://www.notion.so/my-integrations).
    - Garanta que a integração tenha permissão para acessar as páginas que você deseja exportar.
    
- **ID do Banco de Dados ou Página**:
    - Você precisa do ID do banco de dados ou página principal que deseja acessar. O ID pode ser encontrado na URL ao acessar o banco de dados ou página no Notion.

## Como Usar

### 1. Obter o Token da API do Notion

1. Acesse [Notion Developers](https://www.notion.so/my-integrations).
2. Crie uma nova integração.
3. Copie o **token** gerado.

### 2. Obter o ID da Página ou Banco de Dados

1. Vá até a página ou banco de dados que deseja exportar.
2. O ID pode ser encontrado na URL do Notion (exemplo: `https://www.notion.so/{workspace}/{ID-da-página}`).

### 3. Configuração do Script

1. Clone este repositório para o seu ambiente local:

    ```bash
    git clone https://github.com/usuario/notion-to-outline.git
    cd notion-to-outline
    ```

2. Abra o script e insira seu **token de API** e **ID do banco de dados** nas variáveis correspondentes no início do código.

    ```python
    NOTION_API_TOKEN = 'seu_token_aqui'
    DATABASE_ID = 'id_da_sua_base_de_dados'
    ```

3. Instale as dependências necessárias:

    ```bash
    pip install requests
    ```

### 4. Executando o Script

Para gerar o outline, basta rodar o script em seu terminal:

```bash
python notion_to_outline.py
