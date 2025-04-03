# DesenvolvimentoWeb
Fazendo um Projeto com o Django:

1- Criar um projeto django, alterando o nome do arquivo no "Location";

2- Selecionar a caixa "Inherit packages from base interpreter";

3- Depois de Carregar alterar o arquivo settings
	settings: 
		Installed_Apps, Colocando o nome do projeto na última linha, não esquecer a ,
		trocar a linguagem do código

4 -  Após a alteração do arquivo settings, criar o arquivo views dentro da pasta "Manual"

5 - Views:

Importar as bibliotecas: 
	from django.http import HttpResponse
	import os
	from django.shortcuts import render

Criar as funções que o código irá precisar
	exemplo: 
		def index(request):
    animais =[ {'Nome': 'Taquinho', 'Raça': 'Vira-Lata'},
               {'Nome': 'Fofa', 'Raça': 'Vira-Lata'},
               {'Nome': 'Nagi', 'Raça': 'Gato-Amarelo'},
               {'Nome': 'Boneka', 'Raça': 'Vira-Lata'},
    ]
    return render(request, "index.html", {'animais': animais})

6 - Abrir o arquivo urls
    a)Importar
      from . import views  

    b) Incluir a relação entre a função e a página no campo "Urlpatterns"
    	ex:  path('', views.index, name='index'),

7 - Criar o arquivo html em templates, precisa ser o nome que foi definido no arquivo: Views
	a)Configurar o arquivo para que os dados sejam apresentados


