# Eventex

Sistema de Eventos encomendado pela Morena.
Projeto do curso "Welcome to the Django".

[![Build Status](https://travis-ci.org/leogreal/wttd.svg?branch=master)](https://travis-ci.org/leogreal/wttd)
[![Code Health](https://landscape.io/github/leogreal/wttd/master/landscape.svg?style=flat)](https://landscape.io/github/leogreal/wttd/master)
[![Code Climate](https://codeclimate.com/repos/56e00f6580b254141d00ac50/badges/2395869dc4482ff7a17e/gpa.svg)](https://codeclimate.com/repos/56e00f6580b254141d00ac50/feed)
[![Test Coverage](https://codeclimate.com/repos/56e00f6580b254141d00ac50/badges/2395869dc4482ff7a17e/coverage.svg)](https://codeclimate.com/repos/56e00f6580b254141d00ac50/coverage)
[![Issue Count](https://codeclimate.com/repos/56e00f6580b254141d00ac50/badges/2395869dc4482ff7a17e/issue_count.svg)](https://codeclimate.com/repos/56e00f6580b254141d00ac50/feed)

## Como desenvolver

1. Clone o repositorio.
2. Crie um virtualenv com o Python 3.5
3. Ative o virtualenv.
4. Instale as dependências.
5. Configure a instância com o .env
6. Execute os testes.

```console
git clone git@github.com:leogreal/wttd.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
python manage.py test
```

## Como fazer o deploy

1. Crie uma instância no heroku.
2. Envie as configurações para o heroku.
3. Defina uma SECRET_KEY srgura para instância.
4. Defina DEBUG=False
5. Configure o serviço de e-mail.
6. Envie o código para o heroku.

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# Configuro o e-mail
git push heroku master --force
```
