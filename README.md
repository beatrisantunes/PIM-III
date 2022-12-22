<h1 align="center"> PIM - III </h1>

***Curso: Análise e Desenvolvimento de Sistemas - UNIP - 2022***

## 👩🏻‍💻👩🏻‍💻👨🏻‍💻Integrantes:

- 2273384 - BEATRIS ANTUNES SILVA 

- 2292834 - BIANCA ANTUNES SILVA 

- 2292870 - MÁRCIO SANTANA PORTELA

## 📑Descrição do Problema:
O projeto tem o intuito de implementar uma rede de computadores de maneira prática. A 2SHOW.IE, empresa utilizada durante o projeto, decidiu implantar redes de computadores nas duas filiais que possui. Sendo elas um escritório principal e uma sucursal que devem ser interligadas através das redes.

A empresa 2SHOW.IE é uma agência de marketing digital que após um aumento na carteira de clientes e ampliou seu escritório para uma nova unidade, ampliando o espaço e seus serviços.
A empresa solicitou o desenvolvimento de um projeto de interconexão de rede, que dispositivos localizados fisicamente na central comuniquem e compartilhem informações e serviços entre funcionários e usuários.

## 🔗Link:

[Site ](https://www.netacad.com/pt-br/courses/packet-tracer)

## 💻🛠 Tecnologias e Ferramentas:
- Cisco Packet Tracer
- Git e Github

**Será utilizado na plataforma Packet Tracer, para os seguintes equipamentos na sede da unidade:**

- 1 Servidor responsável por manter os serviços DNS;
- 1 Servidor responsável por manter softwares e aplicativos;
- 1 Servidor de páginas de internet;
- 35 Estações de trabalho (host);
- 5 Impressoras multifuncionais em rede;
- 1 Access Point;

**Nova unidade:**

- 1 Servidor responsável por manter os serviços;
- 20 Estações de trabalho;
- 3 Impressoras multifuncionais;
- 1 Access Point.

**Essa conexão deve seguir as seguintes premissas:**

- Configurar um servidor para suportar pelo menos 55 hosts; 
- Conectando roteadores a switches de fábrica com fibra óptica; 
- Reestruturação do endereço IPv4 das redes LAN tanto na matriz quanto nas filiais; 
- Construir o esquema de endereço de rede correto; 
- Certificação de conformidade do projeto com as normas legais gerais.
 
**Fundamentos de redes de dados e Comunicação:**

**Topologia Física:**

<img width="500" src="https://user-images.githubusercontent.com/79115923/209066886-413445ee-da0a-43f1-813b-c7102913c31a.png">

Optamos por utilizar a topologia física em estrela, pois assim distribuímos e o sinal recebido pelo roteador para os dois switches que, por sua vez, distribuem o sinal para as estações de trabalho, os servidores, as multifuncionais e o access point.

**Vantagens de utilizar a topologia física em estrela:**

- Fácil adição na rede, pois se necessário adicionar um novo dispositivo não precisa uma nova codificação;
- Gerenciamento centralizado;
- Caso haja falha em algum dispositivo final não afeta a rede como um todo.

**Desvantagens do uso da topologia em estrela:**

- Caso um dispositivo central falhe, toda a rede será afetada.

## 📌 Resultado:

**Infraestrutura:**

Temos a disposição de como ficariam as redes e sua interligação entre as filiais. 

<img width="500" src="https://user-images.githubusercontent.com/79115923/209064773-a06af007-2d79-48dd-b910-cb9ead36ef2b.png">

**Configurações do Escritório Central:**

Para o escritório central foram usados um roteador, dois switches como dispositivos centrais, um access point, três servidores, cinco multifuncionais e trinta e cinco estações de trabalho.

**Roteador:**

1.	Interface Fast Ethernet 0/0
- Endereço IP: 192.168.0.1 
- Máscara: 255.255.255.0
2.	Interface Fast Ethernet 0/1
- Endereço IP: 192.168.1.1
●	Máscara: 255.255.255.0
- Interface Serial 0/0/0
- Endereço IP: 10.0.0.1 
- Máscara: 255.255.255.252
- Taxa de Clock (Velocidade): 4M
4.	Router Rip
- Rede 10.0.0.0
- Rede 192.168.0.0
- Rede 192.168.1.0

**Servidor DNS, arquivos de usuários e serviço de diretórios:**

1.	Interface Fast Ethernet 0/0
- Endereço IP: 192.168.0.3
- Máscara: 255.255.255.0

**Servidor de softwares e aplicativos de monitoramento de performance, rotinas e pesquisas através da internet:**

1.	Interface Fast Ethernet 0/0
- Endereço IP: 192.168.0.2
- Máscara: 255.255.255.0

**Servidor IIS:**

1.	Interface Fast Ethernet 0/0
- Endereço IP: 192.168.1.2
- Máscara: 255.255.255.0

**Access Point para funcionários:**

1.	Porta de acesso 1
- Encriptação: AES
- Tipo de autenticação: WPA2-PSK
- Password: func_show.ie

**Estações de trabalho e multifuncionais seguiram o padrão de endereçamento IP de cada porta Fast Ethernet que seu switch está conectado no roteador (seguindo a lógica matemática crescente):**

- Sendo os conectados à porta Fast Ethernet 0/0 com os endereços IP: 192.168.0.4 ao 192.168.0.20;
- E os conectados à porta Fast Ethernet 0/1 com os endereços IP: 192.168.1.3 ao 192.168.1.20.

**Configurações da sucursal:**

Para a sucursal foram usados um roteador, um switch e um hub como dispositivos centrais, um access point, um servidor, três multifuncionais e vinte estações de trabalho.

**Roteador:**

1.	Interface Fast Ethernet 0/0
- Endereço IP: 192.168.10.1
- Máscara: 255.255.255.0
2.	Interface Fast Ethernet 0/1
- Endereço IP: 192.168.11.1
- Máscara: 255.255.255.0
3.	Interface Serial 0/0/0
- Endereço IP: 10.0.0.2
- Máscara: 255.255.255.252
- Taxa de Clock (Velocidade): 4M
4.	Router Rip
- Rede 10.0.0.0
- Rede 192.168.10.0
- Rede 192.168.11.0

**Servidor de arquivos dos usuários de impressão:**

1.	Interface Fast Ethernet 0/0
- Endereço IP: 192.168.11.2
- Máscara: 255.255.255.0

**Access Point para funcionários:**
1.	Porta de acesso 1
- Encriptação: AES
- Tipo de autenticação: WPA2-PSK
- Password: func_show.ie

**Estações de trabalho foram conectadas ao switch e seguiram o padrão de endereçamento IP da porta Fast Ethernet 0/0 do roteador em que o switch está conectado (seguindo a lógica matemática crescente):**

- Sendo os conectados à porta Fast Ethernet 0/0 com os endereços IP: 192.168.10.2 ao 192.168.10.21;
- As multifuncionais foram conectadas ao hub junto do servidor de impressão.

**Cabeamento:**

<img width="500" src="https://user-images.githubusercontent.com/79115923/209067048-ebeca41e-67f5-4479-a884-b8e7f4bc8a82.png">

O cabeamento utilizado foi o estruturado horizontal, pois com ele temos a facilidade de instalação para novos equipamentos e uma melhor organização dos cabos utilizados.

**Tipos de cabo:**

Foi utilizado fibra óptica para a interligação das filiais através da contratação de uma empresa distribuidora de sinal de internet.

<img width="500" src="https://user-images.githubusercontent.com/79115923/209067196-ab8d774d-3d20-4ff1-b004-2197d6d444c1.png">

Já para as redes internas das filiais foram utilizados cabos UTP blindados de categoria 6, também chamados de cabos de pares trançados, para a interligação dos dispositivos conectados à rede, tanto do roteador aos switches e hubs, quanto dos switches e hubs para os dispositivos finais, tais como estações de trabalho, servidores e multifuncionais.

<img width="500" src="https://user-images.githubusercontent.com/79115923/209067304-1e5ffd6a-eb2e-4bd8-852b-4e63287dadef.png">

**Protocolo TCP/IP:**

A implementação foi feita utilizando rede de classe C, na qual é possível a conexão de até 254 hosts. Também foi utilizado o protocolo TCP/IP para a configuração dos dispositivos conectados na rede interna das filiais, com máscara de rede 255.255.255.0.

## 🔗Link Parte Escrita:
[Projeto ](https://github.com/beatrisantunes/PIM-III/blob/main/PIM%20III.docx)
