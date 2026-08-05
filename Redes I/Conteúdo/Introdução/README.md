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
