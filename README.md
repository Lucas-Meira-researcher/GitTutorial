# Inicializando nova pasta

* `git init` - Inicializa o repositório

* `git branch -M "main"` -  Alterar o nome da branch principal de `master` para `main` (isso é uma boa prática atualmente recomendada)

* `git remote -v` - Verifica se a pasta está vinculada a um repositório
  
* `git remote add origin <link do repositório>` - Passar o commit do meu repositório local (da minha máquina) para repositório no Github

## Configuração para dataset

* `echo "Pasta com dados/" > .gitignore` - Ignora pasta de dados no git
  
* `cat .gitignore` - Confirma se ta ignorando
  
* `git add .gitignore` - Implementa no Github

* `git commit -m "Adiciona .gitignore para ignorar a pasta de dados"` - Implementa no Github

* `git push origin main` - Implementa no Github
  

# Comandos padrões (Main)

* `git add README.md` para colocar o arquivo na área de stagging 

* `git commit -m "primeiro commit"` - para de fato dar o commit no repositório (pasta)

* `git push -u origin main` - Passa commit da pasta para o git => PRIMEIRA VEZ

 * `git push origin main` - Após primeira vez


# Branch

* `git checkout -b "branch-1"` - Cria branch (Essa realidade paralela pode ser usada para criar outro arquivo ou alterar o arquivo já existente)
 
 * `git checkout main` - Para se mover de uma branch/main para outra

* `git commit -m "Criando branch-1"`

*  `git push origin bramch-1`

# Merge

* `git checkout main`

* `git merge branch-1`

* `git push origin main` - Atualiza no github o merge adicionado à main
