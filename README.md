# Introdução

O Problema do Caixeiro Viajante "tenta determinar a menor rota para percorrer uma série de cidades (visitando uma única vez cada uma delas), retornando à cidade de origem. Ele é um problema de otimização NP-difícil inspirado na necessidade dos vendedores em realizar entregas em diversos locais (as cidades) percorrendo o menor caminho possível..." (Wikipedia, 2020)

Este notebook almeja ilustrar conceitos de aprendizado de máquina aplicados na otimização dos serviços de uma empresa de taxi aéreo fictícia, cujo problema a ser resolvido é similar ao problema do caixeiro viajante.

O algoritmo utiliza heurística construtiva, do tipo 2-opt, codificado em Python, para determinar a rota otimizada dos vôos da empresa aérea.

Antonio Alisio de Meneses Cordeiro (alisio.meneses@gmail.com)

# Mandalore Taxi Aéreo LTDA - This is The Way

## Pitch:

Para organizações com presença nacional, que desejam transportar cargas ou passageiros, A Mandalore Taxi Aéreo LTDA (empresa fictícia), sediada em Fortaleza-CE, é uma empresa de transporte aéreo que opera nos aeroportos de todas as capitais do Brasil. Diferente das empresas que operam de maneira estática e intempestiva, a Mandalore utiliza algoritmo patenteado PCV™ e IoT para criar rotas inteligentes, otimizadas e dinâmicas, para uma série de cidades, retornando à cidade de origem, reduzindo o tempo necessário para a viagem e os custos com transporte e combustível.

## Problema:

A empresa Mandalore foi a vencedora de um processo licitatório aberto pelo governo federal, cujo objeto de contratação é o serviço de logística de transporte por via aérea de abrangência nacional.

A Mandalore precisa coletar 27 switches core de rede em Fortaleza, coincidentemente local da sua sede, e entregar um switch core em cada uma das 27 capitais do Brasil percorrendo o menor caminho possível, reduzindo o tempo necessário para a viagem e os custos inerentes ao transporte e combustível
Â

# Resultado


|index|nome|descricao|latitude|longitude|lat_radians|lon_radians|x|y|
|---|-|--|--|--|--|--|-|-|
|0|0|Fortaleza	Ceará|-3.716640|-38.5423|-0.064868|-0.672690|4972.586968|-323.012994
|1|15|Natal	Rio Grande Do Norte|-5.793570|-35.1986|-0.101117|-0.614331|5179.527247|-525.529930|
|2|11|João Pessoa	Paraíba|-7.115090|-34.8641|-0.124182|-0.608493|5187.215605|-647.489257|
|3|19|Recife	Pernambuco|-8.046660|-34.8771|-0.140441|-0.608720|5175.184638|-731.623024|
|4|13|Maceió	Alagoas|-9.665990|-35.7350|-0.168703|-0.623693|5098.093783|-868.318866|
|5|1|Aracaju	Sergipe|-10.909100|-37.0677|-0.190400|-0.646953|4991.705945|-962.073286|
|6|22|Salvador	Bahia|-12.971800|-38.5011|-0.226401|-0.671971|4858.683044|-1119.196831|
|7|26|Vitória	Espirito Santo|-20.315500|-40.3128|-0.354572|-0.703591|4555.845123|-1686.659544|
|8|21|Rio de Janeiro	Rio de Janeiro|-22.912900|-43.2003|-0.399906|-0.753987|4277.795699|-1808.146751|
|9|9|Florianópolis	Santa Catarina|-27.594500|-48.5477|-0.481615|-0.847317|3737.820630|-1953.628557|
|10|17|Porto Alegre	Rio Grande Do Sul|-30.031800|-51.2065|-0.524154|-0.893722|3455.657802|-1997.683037|
|11|8|Curitiba	Paraná|-25.419500|-49.2646|-0.443654|-0.859829|3755.011488|-1784.576920|
|12|24|São Paulo	São Paulo|-23.532900|-46.6395|-0.410727|-0.814013|4010.440687|-1746.528153|
|13|3|Belo Horizonte	Minas Gerais|-19.910200|-43.9266|-0.347499|-0.766664|4314.308900|-1562.626769|
|14|5|Brasília	Distrito Federal|-15.779500|-47.9297|-0.275404|-0.836531|4107.967426|-1160.850281|
|15|10|Goiânia	Goiás|-16.686400|-49.2643|-0.291233|-0.859824|3982.456984|-1193.764048|
|16|6|Campo Grande	Mato Grosso do Sul|-20.448600|-54.6295|-0.356895|-0.953465|3455.535003|-1288.439481|
|17|7|Cuiabá	Mato Grosso|-15.601000|-56.0974|-0.272289|-0.979084|3422.710611|-955.702368|
|18|20|Rio Branco	Acre|-9.974990|-67.8243|-0.174096|-1.183757|2368.370623|-416.541771|
|19|18|Porto Velho	Rondônia|-8.760770|-63.8999|-0.152904|-1.115264|2770.161155|-426.901645|
|20|14|Manaus	Amazonas|-3.118660|-60.0212|-0.054431|-1.047568|3178.743587|-173.192902|
|21|4|Boa Vista	Roraima|2.823840|-60.6753|0.049285|-1.058984|3116.461620|153.720248|
|22|12|Macapá	Amapá|0.034934|-51.0694|0.000610|-0.891329|4003.399348|2.440926|
|23|2|Belém	Pará|-1.455400|-48.4898|-0.025402|-0.846307|4221.039565|-107.243896|
|24|23|São Luís	Maranhã|-2.538740|-44.2825|-0.044309|-0.772875|4556.560592|-202.030572|
|25|16|Palmas	Tocantins|-10.240000|-48.3558|-0.178722|-0.843968|4166.114878|-752.605416|
|26|25|Teresina	Piauí|-5.091940|-42.8034|-0.088871|-0.747060|4655.889103|-414.866863|
|0|0|Fortaleza	Ceará|-3.716640|-38.5423|-0.064868|-0.672690|4972.586968|-323.012994|

![Rota Renderizada](https://github.com/alisio/mandalore-tsp/blob/master/rota_renderizada.png)

# Referências:

* Baseado no código disponível em https://github.com/Albina1810/TSP
* Informações geográficas disponíveis em https://github.com/kelvins/Municipios-Brasileiros

GEO MIDPOINT. Geographic Midpoint Calculation Example. Disponível em <http://www.geomidpoint.com/example.html>. Acesso em 17 de agosto de 2020.

IBGE. IBGE disponibiliza coordenadas e altitudes para 21.304 localidades brasileiras. Disponível em <https://agenciadenoticias.ibge.gov.br/agencia-sala-de-imprensa/2013-agencia-de-noticias/releases/14126-asi-ibge-disponibiliza-coordenadas-e-altitudes-para-21304-localidades-brasileiras>. Acesso em 17 de agosto de 2020.

PRADO, Kelvin. Github - kelvins/Municipios-Brasileiros. Disponível em <https://github.com/kelvins/Municipios-Brasileiros>. Acesso em 17 de agosto de 2020.

TAYLOR, Roy. Travelling Salesman in scipy
. Disponível em <https://stackoverflow.com/questions/25585401/travelling-salesman-in-scipy>. Acesso em 17 de agosto de 2020

VIASAT. Viasat passa a fornecer internet a bordo para aviões da Aeroméxico .Disponível em <https://viasatdobrasil.com.br/viasat-passa-a-fornecer-internet-a-bordo-para-avioes-da-aeromexico/>. Acesso em 18 de agosto de 2020

WIKIPEDIA. Problema do Caixeiro Viajante. Disponível em <https://pt.wikipedia.org/wiki/Problema_do_caixeiro-viajante>. Acesso em 17 de Agosto de 2020.
