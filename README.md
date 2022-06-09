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


Após isso tem que registrar o aplicativo no projeto

    Como aplicativos e projetos são separadaos no Django, deve registrar o aplicativo no projeto. Atualizando a variável    INSTALLED_APPS dentro de settings.py adicionando uma referencia a classe de configuração do aplicativo.

    A classe esta em apps.py, com o mesmo nome do projeto (no meu caso) HelloWorldConfig


    1. Dentro de helloproject, abra settings.py
    2. Localize a lista INSTALLED_APPS, que deve estar na linha 33
    3. Adicione o seguinte no final da lista

        'hello_world.apps.HelloWorldConfig',
    4. salvar


Entendendo o conceito de CAMINHOS e EXIBIÇÕES
    
    -caminhos
    
    em um aplicativo web, as solicitações do usuário são feitas:

    - Navegando para URLs diferentes
    - Tocando nele
    - Selecionando um link
    - Tocando em um botão

    uma rota informa ao django qual funcão executar, quando o usuário faz uma solicitação para uma URL ou caminho específico

    os caminhos no django são registrados pela configuração de urlpatterns
    esses padrões identificam o que o usuário esta solicitando e determinam qual funcção o django deve tratar a solicitação
    esses padrões são coletados em um módulo que o Django chama de URLconf

    -exibições

    as exibições determinam quais informações devem ser retornadas ao usuário. Elas são funções ou classes que executam o código em resposta a solicitação do usuário.
    elas retornam html


Criar o modo de exibição

    1. abra view.py de dentro aplicativo hello_world
    2. substitua pelo código

        from django.shortcuts import render
        from django.http import HttpResponse

        def index(request):
            return HttpResponse("Hello, World!")

    //a função HttpResponse permite que você retorne texto ou outros tipo primitivos para o chamador



