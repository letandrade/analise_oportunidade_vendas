# Análise de oportunidade de vendas

### 1.0 Descrição
A empresa A-Tech atua no mercado brasileiro de varejo desde 2005. São 45 lojas físicas distribuídas em diferentes regiões. Cada loja possui diversos departamentos, nos quais as vendas acontecem.
<p>Os eventos que acontecem ao longo do ano afetam bastante as vendas, mas cada departamento é afetado de forma diferente. A empresa A-Tech também faz ofertas ao longo do ano sempre antes de eventos importantes. Os principais eventos são: Carnaval (Fevereiro), Independência (Setembro), Black Friday (Novembro) e Natal (Dezembro). As remarcações de preços/descontos que acontecem antes desses eventos impactam as vendas e têm um peso cinco vezes maior na avaliação do que as semanas que não possuem feriado.
<p>A diretora de negócios da A-Tech, Gabriela, deseja reavaliar sua posição no mercado e identificar novas estratégias para se diferenciar da concorrência, melhorando a previsão de como e quais departamentos terão mais oportunidades.
<p>A equipe de dados da A-Tech está totalmente dedicada a um projeto de transformação digital, priorizado pelo CEO, e não poderá realizar estas análises no momento.
<p>O seu time foi selecionado para realizar as análises dos dados disponíveis e apresentar para o time da A-Tech. Sua apresentação servirá de input para o planejamento estratégico da área.
  
### 1.1 Perguntas
  
1. Previsão da demanda – Qual o planejamento de venda das lojas para os próximos 6 meses? Quais as variáveis mais importantes na previsão?
2. Segmentação de lojas - Sabemos que nem todas as lojas são iguais. Algumas lojas têm sazonalidade mais forte, outras são mais afetadas pelos feriados e algumas lojas são afetadas também pela região na qual estão localizadas. O entendimento desses grupos facilita a gestão dos estoques e metas dos gestores. É possível segregar as lojas em grupos? Quais as características
de cada grupo?
  
 ### 2.0 Como usar o projeto
➝ Linguagem Python

➝ Bases em csv
 
 ### 3.0 Desenvolvimento e resultados
Para desenvolver as análises foram importados os datasets "loja.csv", "outras_variaveis.csv" e "vendas.csv" com as seguintes variáveis:
  
  ![image](https://user-images.githubusercontent.com/86376728/229302246-4234837f-6a5d-4ad0-9814-29d87c5bbf9f.png)
  
 A resolução do problema foi dividida nos seguintes tópicos:

### 3.1) Contextualização
Na primeira etapa, busquei entender o que cada variável significava e como elas estavam relacionadas com o problema de negócio. Um ponto importante é que nessa primeira etapa verifiquei que a empresa possui 45 lojas, 99 Departamentos e 3 tipos de lojas. Além disso, percebi que as ações de venda estão alinhadas as datas de eventos e que a companhia sofre efeitos de fatores externos(preço de combustível, IPC, desemprego), esses pontos podem representar oportunidades ou ameaças para o negócio.
  
![image](https://user-images.githubusercontent.com/86376728/229303960-a5690261-56cf-4b6d-8ccd-fefc7bf36c48.png)
  
### 3.2) Segmentação das lojas (Clusterização)
  
Utilizei o modelo K-means para clusterizar as lojas com característica comuns, e através desse modelo, melhorar os resultado de vendas da empresa. Como métrica de performance do cluster foi usado o método do cotovelo. Foram gerados 5 grupos (De 0 a 4), sendo os clusters 0 e 4 os mais relevantes por representarem respectivamente, 36% e 27% do valor de venda. 
  
Os resulatdos do cluster foram aplicados a uma matriz BCG, essa ferramenta permite a compreensão do momento em que cada cluster se apresenta no mercado. Ela é composta por dois eixos, representadas num gráfico: crescimento do mercado (eixo y) e participação relativa (eixo x). Cada eixo, por sua vez, é composto por dois setores, resultando em um quadrante, onde são alocadas as categorias: vaca leiteira, estrela, interrogação e abacaxi. Para melhor entendimento da ferramenta acesse https://www.treasy.com.br/blog/matriz-bcg/
  
  
  ![image](https://user-images.githubusercontent.com/86376728/229304969-9e58ee05-0cb7-41a8-84f6-bdc4e3472cd8.png)
  
 ### 3.3 Modelo de previsão da venda do cluster 0 e do cluster 4
  





