# Analise de vegetação

## Companhia: Bem Agro

### Objetivo do Projeto

Neste projeto possui dois datasets com imagens de setores de uma fazenda da região do Mato Grosso do Sul. O objetivo é baseado nas mesmas, responder as seguintes questões:

- Avaliar se a lavoura está adiantada ou atrasada?
- Existem áreas de recorrência do subdesenvolvimento? É possível detectar essas áreas?
- Existem áreas de subdesenvolvimento exclusivos de uma determinada cultura?
- Além dos datasets, foram fornecidos arquivos CSV. Eles listam algumas variáveis sobre as imagens que estão nos datasets.

Os pontos que serão estudados nesse notebook tem como base resolver as questões acima, com o uso de ferramentas de visão computacional, machine learning e/ou deep learning.

Parte deste dateset são estudos que levam a responder e refletir outros temas relacionado as imagens de satélites disponibilizadas. A outra parte traz uma possível solução que seguem os seguintes passos:

- Entender como é organizado o dataset
- Segmentar as imagens e entender seus índices
- Realizar a classificação das imagens através de seus contornos
- Extrair uma média dos pixels do contorno, obtidas através de bibliotecas de estudo.

No final do processo queremos analisar uma porcentagem de produtividade de cada imagem e compara-las. O que é produtivo, o que não é produtivo e o que é nuvem.

#### Pretenções do projeto

Foram refletidos alguns pontos para resolução das questões:

- Analise sobre volumetria de culturas;
- Analise exploratória sobre NDVI para entendimento se lavoura está adiantada ou atrasada;
- Analise exploratória sobre RGB para entendimento se possuí áreas de subdesenvolvimento (NDVI)
- Clusterização de grupos de imagens por pixels para saber se estão em área de subdesenvolvimento ou não;
- Tendo em mãos o contorno das imagens, podemos extrair uma média das suas cores e criar um gráfico de linhas para entender se temporalmente a lavoura estava adiantada ou atrasada e as sazonalidades das culturas.

### Imagens do dataset

As imagens possuem em seu label sua data, podendo realizar uma análise temporal para entender as diferenças e apontar algum estudo que resolva alguma das questões acima.

O Formato das imagens são RGB e NDVI, os mesmos em seus respectivos diretórios.

O formato RGB é uma escala que possuí três canais(bands) de cores que são Red, Green e Blue. Comparar as imagens com histogramas nessa escala tende a ser mais efetivo para detectar recorrência de áreas de subdesenvolvimento.

O formato NDVI é uma imagem que foi calculada o índice de vegetação, o mesmo é possível analisar a vegetação da localidade e entender melhor sua cultura e monitorar sua lavoura.
A fórmula do cálculo feito para o NDVI é (Infra Vermelho – Vermelho) / (Infra Vermelho +Vermelho)

O princípio teórico é que a vegetação, quanto mais ativa, mais absorve a luz solar na região do vermelho, no processo de trabalho da clorofila nos tecidos vegetais, deixando os valores digitais baixos da imagem de satélite no canal vermelho. Da mesma forma, a estruturas celulares das folhas provocam uma forte reflexão da luz solar na região do Infravermelho próximo (distribuição angular delas e o fator de reflectância bidirecional e outros fatores externos, explica a literatura), deixando os valores digitais altos da imagem de satélite no canal infra vermelho. 

Referência NDVI:
http://www.engesat.com.br/softwares/global-mapper/calculo-do-indice-de-vegetacao-ndvi-no-global-mapper/#:~:text=NDVI%20%C3%A9%20a%20abrevia%C3%A7%C3%A3o%20da,imagens%20geradas%20por%20sensores%20remotos

### Para o futuro

Explorar conectar google earth com dados de chuvas/temporais da região listada e saber se tem interferências em áreas de subdesenvolvimento;

### Desenvolvimento do Projeto

Este projeto foi finalista do Hackaton da bem agro, desenvolvido por eu mesmo, Gabriel Roger :) 

Se você ficou em dúvida, entre em contato comigo :)
