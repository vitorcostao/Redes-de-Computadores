# Redes de Computadores I

A disciplina de Redes de Computadores I tem como foco o estudo dos protocolos e dos métodos utilizados nas redes. Desse modo, os principais objetivos da disciplina são:

1) Demonstrar conceitos relacionados às redes
2) Entender o que são TCP e IP
3) Avaliar OSI
4) Comparar projetos de redes
5) Criar aplicações

---

## Conceitos iniciais

### Rede de computadores

Uma rede de computadores é um conjunto de dispositivos interconectados que se comunicam para compartilhar informações, recursos e serviços. Entre esses dispositivos estão computadores, celulares, impressoras, servidores, roteadores, switches e diversos outros equipamentos.

O principal objetivo de uma rede é permitir a comunicação e o compartilhamento eficiente de dados e recursos entre os dispositivos conectados, garantindo, sempre que necessário, a confidencialidade, a integridade e a disponibilidade das informações transmitidas, princípios fundamentais da segurança da informação.

---

### Modelo de referência OSI

O modelo de referência **OSI (Open Systems Interconnection)** é um modelo conceitual criado para padronizar a comunicação entre computadores em uma rede. Ele divide o processo de comunicação em **7 camadas**, onde cada uma possui uma responsabilidade específica.

1. **Física**
   - **Função:** Transmissão de bits pelo meio físico.
   - **Exemplos:** Cabos, fibras ópticas e sinais elétricos ou de rádio.

2. **Enlace de Dados**
   - **Função:** Comunicação entre dispositivos da mesma rede - Controle de erro, fluxo e enquadramento.
   - **Exemplos:** Ethernet, Wi-Fi (IEEE 802.11) e endereços MAC.

3. **Rede**
   - **Função:** Define o roteamento entre redes.
   - **Exemplos:** IP e ICMP.

4. **Transporte**
   - **Função:** Garante a entrega confiável dos dados e realiza o controle de fluxo.
   - **Exemplos:** TCP e UDP.

5. **Sessão**
   - **Função:** Controla o início, a manutenção e o término das conexões.
   - **Exemplos:** RPC e NetBIOS.

6. **Apresentação**
   - **Função:** Formata, criptografa e comprime os dados.
   - **Exemplos:** SSL/TLS, JPEG e UTF-8.

7. **Aplicação**
   - **Função:** Interface entre os programas e a rede.
   - **Exemplos:** HTTP, HTTPS, FTP, SMTP e DNS.

---


### Arquitetura TCP/IP

A **arquitetura TCP/IP (Transmission Control Protocol/Internet Protocol)** é utilizada na Internet para padronizar a comunicação entre dispositivos em uma rede. Diferente do modelo OSI, ela possui **4 camadas**, cada uma responsável por uma etapa da comunicação.

1. **Acesso à Rede**
   - **Função:** Responsável pela transmissão dos dados no meio físico e pela comunicação entre dispositivos da mesma rede.
   - **Exemplos:** Ethernet, Wi-Fi (IEEE 802.11), PPP.

2. **Internet**
   - **Função:** Responsável pelo endereçamento lógico e pelo roteamento dos pacotes entre diferentes redes.
   - **Exemplos:** IP (IPv4 e IPv6), ICMP, ARP.

3. **Transporte**
   - **Função:** Garante a comunicação entre os processos das aplicações, realizando controle de fluxo, detecção de erros e confiabilidade quando necessário.
   - **Exemplos:** TCP e UDP.

4. **Aplicação**
   - **Função:** Fornece serviços de rede diretamente às aplicações do usuário.
   - **Exemplos:** HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS e DHCP.
  
---


### Modelo Híbrido

O **modelo híbrido** combina características tanto da arquitetura TCP/IP quanto o modelo OSI, tendo, por sua vez, cinco camadas. 

1. **Física**
   - **Função:** Transmissão de bits pelo meio físico.
   - **Exemplos:** Cabos, fibras ópticas e sinais elétricos ou de rádio.

2. **Enlace de Dados**
   - **Função:** Comunicação entre dispositivos da mesma rede - Controle de erro, fluxo e enquadramento.
   - **Exemplos:** Ethernet, Wi-Fi (IEEE 802.11) e endereços MAC.

3. **Rede**
   - **Função:** Define o roteamento entre redes.
   - **Exemplos:** IP e ICMP.

4. **Transporte**
   - **Função:** Garante a entrega confiável dos dados e realiza o controle de fluxo.
   - **Exemplos:** TCP e UDP.

5. **Aplicação**
   - **Função:** Fornece serviços de rede diretamente às aplicações do usuário.
   - **Exemplos:** HTTP, HTTPS, FTP, SMTP, POP3, IMAP, DNS e DHCP.

> OBS: Ao longo da disciplina, será tratado com modelo híbrido

---

## Processo de comunicação em Redes

<img width="1025" height="490" alt="image" src="https://github.com/user-attachments/assets/4c58dbc2-5c59-4a0e-9483-9dad9b9b9bbf" />

A imagem acima ilustra como funciona o processo de comunicação de dispositivos através de redes. Desse modo, cada máquina conectada à rede possui uma pilha de protocolos que podem ser dividida em cinco camadas - 
no caso do modelo híbrido. Nesse cenário, quando há compartilhamento de dados, a máquina fonte irá descer a linha de protocolos que está representado pela linha verde e irá percorrer a rede até chegar no destino, que, 
posteriormente, retornará a resposta seguindo a linha amarela.

Além disso, as máquinas e suas conexões são representadas por grafos, como visualizado na imagem acima Nesse contexto, algumas informações precisam ser ditas. O processo de comunicação é feito por meio de mensagens que, a cada camada, possuem nomes diferentes, além disso cada mensagem possui um cabeçalho e seu conteúdo que, 
ao ser passada, engloba o cabeçalho da mensagem anterior. Logo, tem-se as nomenclaturas:

- **Aplicação**: A mensagem se chama mensagem mesmo.
- **Transporte**: A mensagem se chama segmento.
- **Rede**: A mensagem se chama pacote.
- **Enlace**: A mensagem se chama quadro ou frame.
- **Física**: A mensagem se chama fluxo de bits.

> OBS: Quando uma mensagem desce na pilha de protocolos, ela ganha um cabeçalho. Todavia, quando ela sobe, a mensagem perde um cabeçalho.

### Camadas física, de enlace e de rede, o que fazem?

**Física**: A camada física é responsável por transmitir bits de dados ao longo do processo de comunicação da rede para outras máquinas

**Enlace**: É a camada responsável por enquadrar os dados, isto é, transformar os bits em informação, controlando erros através de Hamming e controlando fluxo.

**Rede**: Na camada de rede, tem-se como principal função o roteamento de pacotes, ou seja, determinar as rotas para onde a mensagem irá. Vale ressaltar que, ao passar por máquinas que não são fonte ou alvo,
a informação atinge até a camada de rede para então encontrar onde ela deve percorrer.

### Camada de Transporte

A camada de transporte é responsável pela **comunicação fim a fim** entre processos (origem e destino).

#### 1. Protocolos Principais

* **TCP (*Transmission Control Protocol*):** Orientado a conexão, com confirmação de entrega de dados.
* **UDP (*User Datagram Protocol*):** Sem conexão, sem garantia ou confirmação de entrega.


#### 2. Endereçamento e Roteamento

* **Endereço IP (Rede):** Utilizado para o **roteamento** dos pacotes entre as máquinas na rede.
* **Endereço de Transporte (Porta):** Utilizado para identificar o **processo/aplicação** específico responsável pela comunicação.


#### 3. Funcionamento dos Segmentos e Portas

* **Serviços por Porta:** Cada serviço ou aplicação em execução na máquina possui uma porta associada.
* **Cabeçalho do Segmento:** Contém as informações de **porta de origem** e **porta de destino**.
* **Inversão de Dados:** Ao responder a uma solicitação, a máquina de destino inverte as informações de IP e porta de origem e destino para encaminhar a resposta de volta ao remetente.

