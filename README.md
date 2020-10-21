# teste-kabug

## Como executar o Projeto

* importante ter o Ruby instalado versão 2.5 ou superior;

### instalar o Bundler

`
gem install bundler
`

### Instalar as dependencias do Ruby (projeto)

`
bundle install
`

### Executar Localmente (Máquina usuário)
`
bundle exec cucumber
`

### Executar no servidor de CI (gerando reports JSON)
`
bundle exec cucumper -p ci
`
