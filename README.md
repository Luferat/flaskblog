# FlaskBlog

Este é um site experimental fullstack feito em [Python](https://www.python.org/), [Flask](https://flask.palletsprojects.com/en/3.0.x/) e [MySQL](https://www.mysql.com/products/community/).

> **IMPORTANTE!** Em todas as interações abaixo, caso o comando `python` não funcione, tente adicionar o número da versão no final. 
> Por exemplo, se o comando `python -version` não funcionar, tente `python3.12 -version`. 
> Se este último funcionar, sempre troque `python` por `python3.12` nos comandos seguintes.

## Visual Studio Code
Se necessário, atualize o VSCode, baixando o instalador da [página oficial](https://code.visualstudio.com/download) ou instalando pela loja do Windows.

Abra o VSCode e instale as extensões iniciais:
 - **[Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)** da Microsoft;
 - **[autopep8](https://marketplace.visualstudio.com/items?itemName=ms-python.autopep8)** da Microsoft;
Se quiser o VSCode em português do Brasil, instale:
 - **[Portuguese (Brazil) Language Pack](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-pt-BR)** da Microsoft.

> Outras  extensões podem ser instaladas quando for necessário.

## Raiz do projeto

Crie uma pasta para o projeto, preferencialmente dentro de "Documentos", por exemplo `Documentos/Python/meuprojeto`.

Abra a pasta do projeto no VSCode.

> Tenha certeza de abrir a pasta que você acabou de criar, no VSCode!!!

## Ambiente virtual

Abra um terminal no VSCode teclando <kbd>Ctrl</kbd> + <kbd>'</kbd> para digitar os próximos comandos.

Crie o ambiente virtual para manter as dependências:
```
python -m venv .venv
```
Ative o ambiente virtual:
```
.venv\Scripts\activate
```
## Dependências

Instale as dependências iniciais:
```
pip install Flask Flask-MySQLdb PyMySQL
```
Gere o arquivo com lista de dependências, `requirements.txt`:
```
pip freeze > requeriments.txt
```
Instalando dependências à partir de `requirements.txt`:
```
pip install -r requeriments.txt
```
> Lembre-se de atualizar a lista de dependências sempre que instalar uma nova dependência no projeto com o comando:
> ```
> pip freeze > requeriments.txt
> ```

## Estrutura do projeto

Crie a estrutura inicial de pastas do projeto:
```
📂 meuprojeto
 └─ 📂 static
     ├─ 📂 css
     ├─ 📂 img
     ├─ 📂 js
    📂 templates
```

Crie o arquivo de entrada da aplicação, responsável por iniciar o servidor:

`index.py`
```
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello World!"

if __name__ == '__main__':
    app.run(debug=True)
```

## Iniciando o servidor

Inicie o servidor Web, embutido no Flask, com o comando:
```
python index.py
```
Não devem ocorrer mensagens de erro e deve ser divulgado o endereço do servidor; provavelmente, `http://127.0.0.1:5000`.
Abra o Google Chrome e acesse esse endereço.
Caso o Chrome seja o navegador padrão, basta clicar no link do terminal para acessar o endereço.

Deve aparecer a mensagem `Hello World!` no navegador, indicando o funcionamento.

## Encerrando

Para interromper o aplicativo:
 - Clique na lata de lixo no menu do terminal para fechá-lo.

ou

 - Tecle <kbd>Ctrl</kbd> + <kbd>C</kbd> para interromper o servidor sem fechar o terminal.

