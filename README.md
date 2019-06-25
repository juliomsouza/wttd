# Eventex
Sistema de eventos encomendado pela Morena.

## Como desenvolver?

1. Clone o repositório.
2. Crie um virtualenv com Python 3.7
3. Ative o virtualenv.
4. Instale as dependencias
5. Configure a instancia com o .env
6. Execute os testes.

''' console
git clone git@github.com:juliomsouza/eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements.txt
cp contrib/env-sample .env
python manage.py test
'''
## Como fazer o deploy?

1. Crie uma instancia no heroku
2. Envie as configurações para o Heroku
3. Defina uma SECRET_KEY para a instancia
4. Defina DEBUG=FALSE
5. Configure o serviço de email.
6. Configure o código para o Heroku

'''console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY='python contrib/secret/secret_gen.py'
heroku config:set DEBUG=False
# configure o email
git push heroku master --force 
 
'''
  