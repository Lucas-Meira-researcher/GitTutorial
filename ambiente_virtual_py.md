# Explicação de como criar um ambiente virtual no python
Isso é importante pois direfentes projetos(scripts) podem usar versões diferentes de uma mesma biblioteca; E ao armazenar todas as bibliotecas num lugar comum, corre-se o risco das verões conflitarem entre si. Os procedimentos à seguir serão feitos usando o git bash

## Entrar na pasta do proejto(script específico)
* `cd /c/Users/Usuario/Desktop/Equidade/relatorio_escolas/relatorio_py`
  * Use `cd` + [diretório]

## Criando o ambiente virtual
* `python -m venv .venv`
  * `-m` -> Executa módulo em python | `venv` -> módulo que cria ambiente virtual | `.venv` nomeia ambiente virtual

## Ativando o ambiente virtual
`source .venv/Scripts/activate`
* `which python python -m pip list`
  *  Confirma se está funcionando:  Caminho deve apontar para) .venv

 ## Instalando bibliotecas
 `python -m pip install` + [Bibliotecas de interesse]
 * `python -m pip install matplotlib numpy pandas reportlab`
   * `python -c "import [Bibliotecas de interesse]; print('Todas as bibliotecas foram encontradas')"` -> Confirmação se deu boa

## Criando requirements.txt
`python -m pip freeze > requirements.txt` 

## Configurando VScode para utilizar ambiente virtual criado
**1. Abra a pasta do projeto no VS Code**
* Clicar em **File** -> Clicar em **Open Folder** -> Selecionar diretório do projeto
 * `cd /c/Users/Usuario/Desktop/Equidade/relatorio_escolas/relatorio_py`

**2. Selecione o ambiente virtual**
2.1 Abra a selção de interpretadores
* Control+Shift+P -> Inserir `Python: Select Interpreter`
2.2 Selecione o ambiente virtual
* Deve aparecer algo como `.venv\Scripts\python.exe`

## Atualizando bibliotecas se faltar alguma para rodar o código:
 * No git bash, retorne à pasta do projeto; ex: `cd /c/Users/Usuario/Desktop/Equidade/relatorio_escolas/relatorio_py`
 * Instala o que faltou diretamente na .venve do projeto; ex: `./.venv/Scripts/python.exe -m pip install [BIBLIOTECAS]`
  * Confirma se instalou certinho: `./.venv/Scripts/python.exe -c "from google.cloud import bigquery; import db_dtypes; print('Bibliotecas instaladas corretamente')"` #Conferir como faz isso direitinho só segui gpt
 * Atualiza requirements: `./.venv/Scripts/python.exe -m pip freeze > requirements.txt`
