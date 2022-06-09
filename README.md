# ms-django
 Roteiro de Aprendizagem - Criar sites controlados por dados usando o Django framework e Python

 Para criar o projeto Django foi utilizado o python 3.

 Para verificar a versão do python

    Windows
    python --version

    Linux
    python3 --version

Para criar uma pasta e entrar na pasta do projeto

    Windows
    md hello_django
    cd hello_django

    Linux
    mkdir hello_django
    cd nello_django

Para criar e ativar o Ambiente Virtual

    Windows
    python -m venv venv
    .\\venv\\Sripts\\Activate

    Linux
    python3 -m venv venv
    source ./venv/bin/activate

Para a instalação do Django (Criar o arquivo requirements.txt)

    Cria um arquivo com o nome requirements.txt
    e dentro do arquivo adicione o texto Django, salve e saia do  arquivo.

    use o comando abaixo para instalar os pacotes que estão dentro do arquivo requirements.txt

    pip install - requirements.txt



O conceito de Mapeamento de URLs

    o mapeamento de url no django é chamado de URLconf e serve como sumário para o aplicativo.
    quando uma URL é solicitada esse módulo localiza o link apropriado dentro do projeto e redireciona a solicitação para o arquivo de exibições contido no aplicativo. A exibição por sua vez, processa a solicitação e executa as operações necessárias.


Criando um projeto com Django-admin

    django-admin startproject helloproject .

    o ponto "." no final a direita significa que o django-admin vai usar a pasta atual. Se você não colocar um subdiretório adicional será criado.


Explicando a estrutura do Projeto

manage.py
helloproject/
    __init__.py
    settings.py
    urls.py
    asgi.py
    wsgi.py


    o manage.py é criado em todos os projetos Django, e tem a mesma função do django-admin

    para visualizar utilize "python manage.py help" para visualizar os comandos


    - helloproject é considerado o pacote de Python de seu projeto
    - init.py é um arquivo vazio que funciona para dizer ao Python que esse diretório deve ser considerado um pacote.
    - setting.py contém todas as configurações ou definições
    - urls.py contém as URLs dentro do projeto
    - asgy.py e wsgi.py servem como ponto de entrada paa os servidores Web dependendo do tipo de servidor implantado.

Executar o Projeto

    python manage.py runserver

Verificar se esta Funcionando

    http://localhost:8000

e para Parar o servidor

    Ctrl + C


Criando o aplicativo Olá Mundo

    Nessa parte vamos entender como os aplicativos são criados e como eles funcionam com o projeto Django


    python manage.py startapp hello_world


    Com esse comando o Django cria as pastas e arquivos necessários, e a estrutura a seguir deve estar visível

    hello_world/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py

