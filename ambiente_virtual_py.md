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
