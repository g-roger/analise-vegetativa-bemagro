# Analise de vegetação

## Companhia: Bem Agro (hackaton)

### Objetivo do Projeto

Este projeto utiliza dois datasets contendo imagens de setores de uma fazenda na região do Mato Grosso do Sul. O objetivo é utilizar ferramentas de visão computacional, machine learning e/ou deep learning para responder as seguintes questões:

- Avaliar se a lavoura está adiantada ou atrasada.
- Detectar áreas de recorrência do subdesenvolvimento e determinar se é possível identificar essas áreas.
- Identificar áreas de subdesenvolvimento exclusivas de uma determinada cultura.
- Utilizar os arquivos CSV fornecidos, que listam variáveis sobre as imagens nos datasets, para obter informações relevantes.

Este notebook aborda os pontos acima mencionados e fornece uma solução possível em quatro etapas:

- Compreender como o dataset está organizado.
- Segmentar as imagens e compreender seus índices.
- Realizar a classificação das imagens com base em seus contornos.
- Extrair uma média dos pixels do contorno utilizando bibliotecas de estudo.

Ao final do processo, será possível analisar a produtividade de cada imagem e compará-las. Será possível determinar quais são produtivas, quais não são - produtivas e quais contêm nuvens. Além de responder às questões acima mencionadas, este projeto também pode ser utilizado para estudar outros temas relacionados a imagens de satélite.

#### Pretenções do projeto

Para a resolução das questões, foram considerados os seguintes pontos:

- Análise de volumetria das culturas: Além de avaliar o volume das culturas, é importante verificar sua distribuição espacial para identificar possíveis problemas de desenvolvimento em áreas específicas da lavoura.
- Análise exploratória do NDVI para determinar se a lavoura está adiantada ou atrasada: Essa análise pode ajudar a avaliar a saúde das plantas e se a lavoura está em uma fase avançada ou atrasada em relação ao ciclo de crescimento esperado.
- Análise exploratória do RGB para detectar áreas de subdesenvolvimento (NDVI): O uso de imagens de cores RGB pode ajudar a identificar áreas com baixa produtividade ou com problemas de desenvolvimento, que podem ser associadas a baixos valores de NDVI.
- Clusterização de grupos de imagens por pixels para identificar áreas de subdesenvolvimento: A técnica de clusterização pode ajudar a agrupar pixels com características semelhantes, permitindo a identificação de áreas de subdesenvolvimento da lavoura.
- Cálculo da média das cores e criação de um gráfico de linhas para entender o desenvolvimento temporal da lavoura: Essa técnica permite avaliar o progresso temporal da lavoura em relação ao esperado, identificando possíveis problemas de desenvolvimento e sazonalidades das culturas.

### Imagens do dataset

As imagens contêm em seus rótulos a data correspondente, permitindo a análise temporal para identificar diferenças e propor estudos que abordem as questões levantadas anteriormente.

As imagens são fornecidas em dois formatos: RGB e NDVI, cada um armazenado em seu respectivo diretório.

O formato RGB é uma escala de cores composta por três canais (red, green e blue). A análise de histogramas nesta escala pode ser mais eficaz para identificar áreas de subdesenvolvimento recorrentes.

O formato NDVI é uma imagem que representa o índice de vegetação e permite a análise da cobertura vegetal da região, proporcionando uma melhor compreensão da cultura local e a monitoração das lavouras. A fórmula utilizada para calcular o NDVI é (Infravermelho - Vermelho) / (Infravermelho + Vermelho).

O princípio teórico subjacente é que a vegetação ativa absorve mais luz solar na região do vermelho, devido ao processo de trabalho da clorofila nos tecidos vegetais, o que resulta em valores digitais baixos na imagem de satélite no canal vermelho. Da mesma forma, as estruturas celulares das folhas refletem fortemente a luz solar na região do infravermelho próximo (a distribuição angular das folhas e o fator de refletância bidirecional, entre outros fatores externos, explicam essa reflexão), resultando em valores digitais elevados na imagem de satélite no canal infravermelho.


Referência NDVI:
http://www.engesat.com.br/softwares/global-mapper/calculo-do-indice-de-vegetacao-ndvi-no-global-mapper/#:~:text=NDVI%20%C3%A9%20a%20abrevia%C3%A7%C3%A3o%20da,imagens%20geradas%20por%20sensores%20remotos

### Perspectivas Futuras

Uma ideia interessante é explorar a conexão do Google Earth com os dados de chuva/temporal da região para identificar possíveis interferências nas áreas de subdesenvolvimento.

### Desenvolvimento do Projeto

Este projeto foi desenvolvido por mim, Gabriel Roger, e foi um dos finalistas do Hackathon da Bem Agro. Caso tenha alguma dúvida ou queira mais informações, sinta-se à vontade para entrar em contato comigo.
