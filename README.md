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

