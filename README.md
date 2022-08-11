# Teste Técnico Lucas Pigoso - Letrus

## Fase 1

Para esta etapa foi necessário todo desenvolvimento por trás da criação do banco de dados assim como do dashboard.

Em se tratando do **banco de dados**, não haviam informações para popular as tabelas *Sexo*, *Ativo* e *Endereço*, portanto estabeleci como convenção os valores baixo:

TB *Sexo*
![image](https://user-images.githubusercontent.com/33936130/184216010-edbc9337-a4f9-4cf0-bb30-cc3b9c16e9e6.png)

TB *Ativo*
![image](https://user-images.githubusercontent.com/33936130/184216166-ba6dfc8b-59ef-4137-be3a-7eaa5d56b6ef.png)

Já para a tabela *Endereço* usei valores gerados aleatoriamente por meio de Google + Excel

- Os relatórios solicitados (dashboard) encontram-se no Pdf **_DataStudio Letrus - Filtrado_** e também podem ser acessados por meio do [[link](https://datastudio.google.com/reporting/c081106b-eb0e-41fe-bff3-50d77afc4a74)]. É possível perceber que os gráficos não estão filtrados (também em pdf **_DataStudio Letrus - Default_**), ou seja, não filtrei as queries pois me parece mais interessante, do ponto de vista do usuário, ter escalabilidade para filtrar da forma que achar ideal.

- Já as alterações (exclusões, edições, views) eu realizei por meio de queries, estou disponibilizando-as no arquivo **_Fase 3 - Queries.txt_** e fazem parte do que está solicitado na Fase 3. Caso seja necessário acesso ao banco de dados, vou deixá-lo no e-mail respectivo ao teste.


## Fase 2

(Todas as imagens abaixo possuem a respectiva query disponilizada no arquivo texto)

1. Para auxiliar os professores a terem uma visão panorâmica, entendo que é importante terem um comparativo de quais projetos possuem atividades com baixas notas, pois acaba sendo um indicativo de que deve-se olhar mais de perto esses projetos. Desta forma, criei duas views que podem auxiliar nesse sentido:

Visão geral de atividade por atividade, nota a nota

![image](https://user-images.githubusercontent.com/33936130/184224053-c8878292-d8a6-409a-94aa-da6e6278e800.png)

Visão geral dos projetos, já calculado a média das notas
![image](https://user-images.githubusercontent.com/33936130/184224745-c39f72d9-3b48-4d53-9159-c176384afaf3.png)


## Fase 3

Como já citado acima, os arquivos para esta etapa - com todas as queries que foram utilizadas- encontram-se em **_Fase 3 - Queries.txt_**
