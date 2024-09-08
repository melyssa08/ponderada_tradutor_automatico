## Tradução Automática

A partir do exercício feito, que no caso é "9.5. Tradução Automática e o Conjunto de Dados". As respostas para a seção "9.5.7" estão logo abaixo:

Primeira pergunta "Tente valores diferentes do argumento num_examples na funçãoload_data_nmt. Como isso afeta os tamanhos do vocabulário do idioma de origem e do idioma de destino?":

Quando foram testados 700 exemplos em comparação com o valor padrão de 600, observou-se um aumento no vocabulário de origem e destino. Isso ocorreu porque o modelo encontrou mais palavras únicas com um maior número de exemplos, enriquecendo o vocabulário. No entanto, ao reduzir o número de exemplos para 500, o vocabulário também diminuiu, uma vez que o modelo encontrou menos palavras únicas. Em outras palavras, um maior número de exemplos resulta em um vocabulário mais amplo e variado, permitindo uma tradução mais precisa ao capturar uma gama maior de nuances linguísticas. O equilíbrio entre a quantidade de exemplos e o tamanho do vocabulário é crucial para otimizar o desempenho do modelo de tradução.

Obs: Os valores de tamanho de vocabulários são vistos dentro do notebook, na descrição acima está uma análise comparativa;

Segunda pergunta "O texto em alguns idiomas, como chinês e japonês, não tem indicadores de limite de palavras (por exemplo, espaço). A tokenização em nível de palavra ainda é uma boa ideia para esses casos? Por que ou por que não?":

A segmentação de palavras em chinês e japonês não pode ser baseada no uso de espaços, como ocorre em idiomas como o inglês, uma vez que espaços não são uma característica comum nesses idiomas. Para lidar com essa dificuldade, técnicas de segmentação devem considerar o contexto gramatical e estrutural das sentenças [1].
Empresas como a IBM desenvolvem métodos avançados para enfrentar esse desafio [2], empregando algoritmos de segmentação que utilizam aprendizado de máquina e regras linguísticas, apoiados por dicionários e corpora específicos para cada idioma. Modelos estatísticos e baseados em regras são treinados com grandes volumes de dados reais para aprimorar a precisão da segmentação, levando em conta a frequência e a co-ocorrência de caracteres.
Além disso, técnicas de normalização de caracteres e pré-processamento são aplicadas para assegurar consistência e qualidade no texto segmentado. A capacidade de processamento multilíngue dessas abordagens permite a segmentação eficiente de chinês e japonês, adaptando-se às especificidades de cada idioma.
Portanto, embora a segmentação nesses idiomas não siga o mesmo método do inglês, é possível alcançar uma segmentação eficaz através da consideração do contexto e da aplicação de técnicas avançadas.

Referências:

[1] Tatsuya Hiraoka, Hiroyuki Shindo, and Yuji Matsumoto. 2019. Stochastic Tokenization with a Language Model for Neural Text Classification. In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics, pages 1620–1629, Florence, Italy. Association for Computational Linguistics.

[2] https://www.ibm.com/docs/pt/i/7.3?topic=processing-chinese-japanese-korean