# Lista 1 - Unidade I - Introdução à Arquitetura TCP/IP

## 1) Quais são as funções das sete camadas do modelo de referência OSI?

As sete camadas do modelo OSI possuem funções diferentes no processo de comunicação:

- **Física:** transmite os bits pelo meio físico, como cabos, fibras e sinais de rádio.
- **Enlace:** controla a comunicação entre dispositivos diretamente conectados, organizando os dados em quadros e utilizando endereços MAC.
- **Rede:** determina o caminho dos dados entre diferentes redes, utilizando endereços IP e realizando o roteamento.
- **Transporte:** garante a comunicação entre aplicações, podendo controlar a entrega, a ordem e a confiabilidade dos dados.
- **Sessão:** estabelece, mantém e encerra as sessões de comunicação entre aplicações.
- **Apresentação:** trata da representação dos dados, incluindo conversão de formatos, criptografia e compressão.
- **Aplicação:** fornece serviços de rede diretamente às aplicações do usuário, como HTTP, DNS e FTP.

---

## 2) Qual a diferença de visibilidade entre as camadas de rede e enlace?

A camada de enlace tem uma visibilidade mais local, pois trabalha com a comunicação entre dispositivos diretamente conectados na mesma rede, usando endereços MAC. Já a camada de rede possui uma visão mais ampla, sendo responsável por levar os dados entre redes diferentes, usando endereços IP e realizando o roteamento.

---

## 3) Tanto a camada de rede quanto a de transporte, são responsáveis pela transferência de dados, qual é a diferença entre elas?

A camada de rede é responsável por levar os dados entre diferentes dispositivos e redes, utilizando endereços IP e definindo o caminho que os pacotes devem seguir. Já a camada de transporte é responsável pela comunicação entre as aplicações desses dispositivos, garantindo, quando necessário, a entrega, a ordem e a confiabilidade dos dados.

---

## 4) O que significa Broadcasting na camada de rede e na de enlace?

Broadcasting significa a transmissão de dados para todos os dispositivos de uma determinada rede.

Na camada de enlace, o broadcast é feito usando um endereço MAC de destino especial, permitindo que todos os dispositivos da rede local recebam o quadro. Na camada de rede, o broadcast utiliza um endereço IP de broadcast para enviar o pacote a todos os dispositivos da mesma rede.

---

## 5) Em breve, teremos um terminal doméstico e seguro conectado à Internet permitindo plebiscitos instantâneos sobre questões importantes. Nesse caso, a política atual será eliminada. Os aspectos positivos dessa democracia direta são óbvios. Apresente alguns dos aspectos negativos.

Alguns pontos negativos seriam a possibilidade de as pessoas tomarem decisões sem conhecer bem o assunto, principalmente quando se trata de questões complexas. Além disso, a opinião pública poderia ser facilmente influenciada por notícias falsas, campanhas ou grupos com maior poder de comunicação.

Outro problema é que muitas decisões poderiam ser tomadas por emoção ou por acontecimentos do momento, sem pensar nas consequências a longo prazo. Também existe o risco de os interesses das minorias serem deixados de lado, já que a maioria sempre teria mais influência. Por fim, se houvesse muitos plebiscitos, as pessoas poderiam ficar cansadas e perder o interesse em participar das decisões.

---

## 6) O presidente da XBeer resolve trabalhar com a YBeer para produzir uma lata de cerveja invisível (medida higiênica). O presidente pede que o jurídico analise a questão. Esse contacta o departamento de Engenharia. Como resultado, o engenheiro-chefe entra em contato com seu par na YBeer para discutirem os aspectos técnicos. Em seguida, os engenheiros enviam um relatório aos departamentos jurídicos, que discutem os aspectos legais. Por fim, os presidentes discutem as questões financeiras do negócio. Esse é um exemplo de protocolo em várias camadas no sentido utilizado pelas redes de computadores? Justifique.

Esse é um exemplo de protocolo em várias camadas, pois cada nível da empresa se comunica com o nível correspondente da outra empresa, seguindo uma ordem específica.

Primeiro, os presidentes tratam das questões gerais e financeiras. Depois, os departamentos jurídicos analisam os aspectos legais e, por fim, os engenheiros discutem os aspectos técnicos. Cada camada possui uma função específica e se comunica com a camada equivalente da outra empresa.

Isso é semelhante às redes de computadores, onde cada camada possui suas próprias responsabilidades e se comunica logicamente com a mesma camada do outro dispositivo, enquanto utiliza os serviços das camadas inferiores.

---

## 7) Um sistema tem uma hierarquia de protocolos com n camadas. As aplicações geram mensagens com M bytes de comprimento. Em cada uma das camadas, é acrescentado um cabeçalho com h bytes. Qual é a fração dos dados enviados que corresponde ao tamanho dos cabeçalhos?

Se temos **n camadas** e cada camada adiciona um cabeçalho de **h bytes**, então o tamanho total dos cabeçalhos será:

**n · h**

A mensagem original possui **M bytes**, então o tamanho total enviado será:

**M + n · h**

Portanto, a fração dos dados enviados que corresponde aos cabeçalhos é:

**(n · h) / (M + n · h)**

Ou seja, basta dividir o total de bytes dos cabeçalhos pelo total de bytes enviados.

---

## 8) Determine qual das camadas do modelo TCP/IP trata de cada uma das tarefas a seguir:

**a)** Dividir o fluxo de bits transmitidos em quadros → **Camada de Enlace.**

**b)** Definir a rota que será utilizada na sub-rede → **Camada de Rede (Internet).**

---

## 9) Cite dois aspectos em que os modelos de referência OSI e TCP/IP são similares e dois em que eles são diferentes

### Semelhanças

- Ambos possuem uma arquitetura em camadas, dividindo as funções da comunicação em diferentes níveis.
- Ambos possuem camadas responsáveis por funções semelhantes, como rede e transporte.

### Diferenças

- O OSI possui 7 camadas, enquanto o TCP/IP possui 4 camadas.
- O modelo OSI separa as camadas de sessão e apresentação, enquanto no TCP/IP essas funções ficam agrupadas na camada de aplicação.

---

## 10) Diferencie os protocolos TCP e UDP

O TCP é orientado à conexão e garante maior confiabilidade na transmissão dos dados, verificando se os pacotes chegaram corretamente e na ordem certa. Por isso, é mais seguro, mas também pode ser mais lento.

O UDP não estabelece uma conexão e não garante que os dados chegarão ou estarão na ordem correta. Em compensação, possui menos overhead e é mais rápido.

---

## 11) Explique os termos Latência, Largura de Banda e Taxa de Dados

- **Latência:** é o tempo que um dado leva para ir de um ponto a outro na rede. Quanto menor a latência, mais rápida é a resposta.
- **Largura de banda:** é a capacidade máxima de transmissão de dados de uma conexão, geralmente medida em bits por segundo (bps).
- **Taxa de dados:** é a quantidade de dados que realmente está sendo transmitida por unidade de tempo, também medida em bps.

---

## 12) Uma sonda localizada na Lua, a uma distância média de 360.000 km da Terra, precisa transmitir um arquivo de 54 MBytes para o centro de controle da NASA. Considerando que o link de comunicação possui uma taxa de transmissão de 2 Mbps e que a velocidade dos sinais é de 3×10⁸ m/s, calcule o tempo necessário para completar a transferência do arquivo.

O arquivo possui **54 MBytes**, que correspondem a **432 Mbits**. Como a taxa de transmissão é de **2 Mbps**, o tempo necessário para transmitir o arquivo é de:

**432 ÷ 2 = 216 segundos.**

Além disso, é necessário considerar o tempo que o sinal leva para percorrer a distância entre a Lua e a Terra. Como a distância é de **360.000 km** e a velocidade do sinal é de **3×10⁸ m/s**, esse tempo é de **1,2 segundo**.

Portanto, o tempo total para completar a transferência é de **217,2 segundos**, aproximadamente **3 minutos e 37 segundos**.
