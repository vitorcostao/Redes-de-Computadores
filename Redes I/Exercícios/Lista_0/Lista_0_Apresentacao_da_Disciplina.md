# Lista 0 - Apresentação da disciplina (Exercícios)

## 1) Quais são as sete camadas do modelo de referência OSI?

- Física
- Enlace
- Rede
- Transporte
- Sessão
- Apresentação
- Aplicação

---

## 2) Qual a diferença de visibilidade entre as camadas de rede e enlace?

A camada de enlace tem uma visibilidade mais local, pois trabalha com a comunicação entre dispositivos diretamente conectados na mesma rede, usando endereços MAC. Já a camada de rede possui uma visão mais ampla, sendo responsável por levar os dados entre redes diferentes, usando endereços IP e realizando o roteamento.

---

## 3) Tanto a camada de rede quanto a de transporte são responsáveis pela transferência de dados. Qual a diferença entre elas?

A camada de rede é responsável por levar os dados de uma rede para outra, definindo o caminho que os pacotes devem seguir usando endereços IP. Já a camada de transporte garante a comunicação entre as aplicações dos dispositivos, podendo controlar a entrega, a ordem e a confiabilidade dos dados.

---

## 4) O que significa Broadcasting na camada de rede e na de enlace?

Broadcasting significa a transmissão de dados para todos os dispositivos de uma determinada rede.

Na camada de enlace, o broadcast é feito usando um endereço MAC de destino especial, permitindo que todos os dispositivos da rede local recebam o quadro. Na camada de rede, o broadcast utiliza um endereço IP de broadcast para enviar o pacote a todos os dispositivos da mesma rede.

---

## 5) No caso da rede de difusão, discuta as vantagens e desvantagens da alocação estática, dinâmica centralizada e dinâmica descentralizada ou distribuída.

Na rede de difusão, vários dispositivos compartilham o mesmo meio de transmissão. A alocação define quem pode transmitir e quando.

- **Alocação estática:** cada dispositivo recebe uma parte fixa do canal. É simples e previsível, mas pode desperdiçar capacidade quando alguns dispositivos não têm dados para transmitir.

- **Alocação dinâmica centralizada:** um dispositivo central controla quem pode transmitir. Aproveita melhor o canal e evita conflitos, mas o dispositivo central pode se tornar um ponto de falha ou gargalo.

- **Alocação dinâmica descentralizada/distribuída:** os próprios dispositivos decidem quando transmitir, seguindo regras de acesso ao meio. Não depende de um controlador central e é mais flexível, mas pode haver colisões e é mais complexa de controlar.
