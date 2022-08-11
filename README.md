# Teste Técnico Lucas Pigoso - Letrus

## Fase 1

Para esta etapa foi necessário todo desenvolvimento por trás da criação do banco de dados assim como do dashboard.

Em se tratando do **banco de dados**, não haviam informações para popular as tabelas *Sexo*, *Ativo* e *Endereço*, portanto estabeleci como convenção os valores baixo:

TB *Sexo*

![image](https://user-images.githubusercontent.com/33936130/184216010-edbc9337-a4f9-4cf0-bb30-cc3b9c16e9e6.png)

TB *Ativo*

![image](https://user-images.githubusercontent.com/33936130/184216166-ba6dfc8b-59ef-4137-be3a-7eaa5d56b6ef.png)

Já para a tabela *Endereço* usei valores gerados aleatoriamente por meio de Google + Excel

- Os relatórios solicitados (dashboard) encontram-se no Pdf [**_DataStudio Letrus - Filtrado_**](https://github.com/LPigoso/letrus/blob/main/DataStudio%20Letrus%20-%20Filtrado.pdf) e também podem ser acessados por meio do [link](https://datastudio.google.com/reporting/c081106b-eb0e-41fe-bff3-50d77afc4a74). É possível perceber que os gráficos não estão filtrados (também em pdf [**_DataStudio Letrus - Default_**](https://github.com/LPigoso/letrus/blob/main/DataStudio%20Letrus%20-%20Default.pdf)), ou seja, não filtrei as queries pois me parece mais interessante, do ponto de vista do usuário, ter escalabilidade para filtrar da forma que achar ideal.

- Já as alterações (exclusões, edições, views) eu realizei por meio de queries, estou disponibilizando-as no arquivo **_Fase 3 - Queries.txt_** e fazem parte do que está solicitado na Fase 3. Caso seja necessário acesso ao banco de dados, vou deixá-lo no e-mail respectivo ao teste.


## Fase 2

(Todas as imagens abaixo possuem a respectiva query disponilizada no arquivo texto)

**1.** Para auxiliar os professores a terem uma visão panorâmica, entendo que é importante terem um comparativo de quais projetos possuem atividades com baixas notas, pois acaba sendo um indicativo de que deve-se olhar mais de perto esses projetos. Desta forma, criei duas views que podem auxiliar nesse sentido:

Visão geral de atividade por atividade, nota a nota

![image](https://user-images.githubusercontent.com/33936130/184224745-c39f72d9-3b48-4d53-9159-c176384afaf3.png)

Visão geral dos projetos, já calculado a média das notas

![image](https://user-images.githubusercontent.com/33936130/184224053-c8878292-d8a6-409a-94aa-da6e6278e800.png)


**2.**  Para dar melhor visiblidade de engajamento, podemos analisar como os projetos se comportam em relação aos outros, assim como de que forma evoluem ano a ano:

![image](https://user-images.githubusercontent.com/33936130/184226648-6456c6ba-e131-415b-a264-946c62147b1e.png)

- Caso fosse inserido em dashboard, poderíamos ter algo como:
(Para este dash, filtrei apenas 3 projetos, porém esse filtro poderia ser feito de forma livre, de forma a podermos entender quais projetos possuem maior alcance e crescimento de forma relativa)

![Atividades por periodo](https://user-images.githubusercontent.com/33936130/184227213-05067d25-c7c9-4ff9-bad3-e79db3e6dc56.png)

Também podemos notar quais cidades possuem maior aderência. (Neste caso, entendo que as cidades são respectivas ao _usuario_, pois na tabela **endereço** temos a coluna _id_usuario_ para correlacionar):

![image](https://user-images.githubusercontent.com/33936130/184227297-842fee8f-ab5d-42cc-8c03-15016eb1c877.png)

**3.** Sobre padrões e anomalias, há algumas situações que pude notar durante a prática. Como:

- Os projetos, apesar de conterem id, sem nome definidos;
- Os projetos que estão relacionados a id_usuario inexistente - não há usuários com id acima de 1500, porém a maioria dos projetos se relaciona com um id maior que este valor;
- As atividades possuem valor de coluna id_projeto até o valor 49, porém temos 1500 projetos, ou seja, não é possível fazer o relacionamento entre a maioria deles;
- As atividades possuem valor de coluna id_projeto 0, porém não há existência desse projeto; entre outros

Além disso, podemos procurar por padrões/anomalias de forma estatística. Através de Python, realizei uma construção bem simples, que permite visualizarmos o comportamento das notas (tabela **notas**). Há inúmeras outras análises estatísticas que podem ser realizadas nesta e em outras tabelas:

- Histograma de notas finais: podemos através dele como estão distribuídas as notas finais. Percemos que ocorre de alguma forma "binária", portanto, esse valor acaba sendo 0 ou 10, com exceção dos casos de valor nulo. Também notamos como há maior frequência de valores 10

![Histograma notas finais](https://user-images.githubusercontent.com/33936130/184229926-c844d481-7d18-4b1d-83f4-f00b6a4941da.png)

- Boxplot das notas 1, 2, 3 e 4: percebemos que não há outliers e que as notas se comportam de forma semelhante, acabamos vendo que há um comportamento "padrão" que não contem inconsistências.

![Boxplot notas](https://user-images.githubusercontent.com/33936130/184229939-c3165b22-f292-47ca-a46b-f92f809b3d40.png)


## Fase 3

Como já citado acima, os arquivos para esta etapa - com todas as queries que foram utilizadas- encontram-se em **_Fase 3 - Queries.txt_**
