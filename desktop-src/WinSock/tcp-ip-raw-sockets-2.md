---
description: Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: Soquetes brutos TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25cc08d59d80089a4e655f363e4a899edac8d2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808210"
---
# <a name="tcpip-raw-sockets"></a>Soquetes brutos TCP/IP

Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. Este tópico se concentra apenas em soquetes brutos e protocolos IPv4 e IPv6. Isso ocorre porque a maioria dos outros protocolos com exceção de ATM não oferece suporte a soquetes brutos. Para usar soquetes brutos, um aplicativo precisa ter informações detalhadas sobre o protocolo subjacente que está sendo usado.

Provedores de serviço Winsock para o protocolo IP podem dar suporte a um *tipo* de soquete de **Sock \_ RAW**. O provedor do Windows Sockets 2 para TCP/IP incluído no Windows dá suporte a esse tipo de soquete **\_ bruto Sock** .

Há dois tipos básicos desses soquetes brutos:

-   O primeiro tipo usa um tipo de protocolo conhecido gravado no cabeçalho IP que é reconhecido por um provedor de serviços do Winsock. Um exemplo do primeiro tipo de soquete é um soquete para o protocolo ICMP (tipo de protocolo IP = 1) ou o protocolo ICMPv6 (IP Procotol Type = 58).
-   O segundo tipo permite que qualquer tipo de protocolo seja especificado. Um exemplo do segundo tipo seria um protocolo experimental que não é suportado diretamente pelo provedor de serviços do Winsock, como o SCTP (Stream Control transmiting Protocol).

## <a name="determining-if-raw-sockets-are-supported"></a>Determinando se há suporte para soquetes brutos

Se um provedor de serviços Winsock oferecer suporte a soquetes **\_ brutos Sock** para as \_ famílias de endereços INET6 inet ou AF \_ , o tipo de soquete de **Sock \_ bruto** deverá ser incluído na estrutura de [**\_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) retornada pela função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) para um ou mais dos provedores de transporte disponíveis.

O membro **iAddressFamily** na estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) deve especificar a INET6 de AF \_ ou AF \_ , e o membro **ISocketType** da estrutura de **\_ informações WSAPROTOCOL** deve especificar **Sock \_ RAW** para um dos provedores de transporte.

O membro **iProtocol** da estrutura [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pode ser definido como **IPROTO \_ IP**. O membro **iProtocol** da estrutura **de \_ informações de WSAPROTOCOL** também poderá ser definido como zero se o provedor de serviços permitir que um aplicativo use um tipo de soquete **\_ bruto Sock** para outros protocolos de rede que não sejam o protocolo de Internet para a família de endereços.

Os outros membros na estrutura [**de \_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) indicam outras propriedades do suporte de protocolo para **Sock \_ RAW** e indicam como um soquete de **Sock \_ bruto** deve ser tratado. Esses outros membros das **\_ informações de WSAPROTOCOL** para o **Sock \_ RAW** normalmente especificam que o protocolo é sem conexão, orientado a mensagens, dá suporte à difusão/multicast (o XP1 sem \_ conexão e à \_ mensagem XP1, a difusão de suporte a \_ XP1 e os bits do MultiPoint com \_ \_ \_ suporte \_ são definidos no membro XP1) e pode ter um tamanho máximo de mensagem de 65.467 bytes.

No Windows XP e posterior, o comando *NetSh.exe* pode ser usado para determinar se há suporte para soquetes brutos. O comando a seguir executado de uma janela CMD exibirá dados do catálogo Winsock no console:

**netsh winsock mostrar catálogo**

A saída incluirá uma lista que contém alguns dos dados das estruturas de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) com suporte no computador local. Procure o termo RAW/IP ou RAW/IPv6 no campo Descrição para localizar os protocolos que oferecem suporte a soquetes brutos.

## <a name="creating-a-raw-socket"></a>Criando um soquete bruto

Para criar um soquete do tipo **Sock \_ RAW**, chame a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ou [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) com o parâmetro *AF* (família de endereços) definido como \_ AF inet ou AF \_ INET6, o parâmetro de *tipo* definido como **Sock \_ RAW** e o parâmetro de *protocolo* definido como o número de protocolo necessário. O parâmetro de *protocolo* se torna o valor de protocolo no cabeçalho IP (SCTP é 132, por exemplo).

> [!Note]  
> Um aplicativo não pode especificar zero (0) como o parâmetro de *protocolo* para as funções [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket), [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)e [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) se o parâmetro de *tipo* estiver definido como **Sock \_ RAW**.

 

Os soquetes brutos oferecem a capacidade de manipular o transporte subjacente, para que possam ser usados para fins mal-intencionados que apresentam uma ameaça à segurança. Portanto, somente os membros do grupo Administradores podem criar soquetes do tipo SOCK \_ RAW no Windows 2000 e posterior.

## <a name="send-and-receive-operations"></a>Operações de envio e recebimento

Quando um aplicativo cria um soquete do tipo **Sock \_ RAW**, esse soquete pode ser usado para enviar e receber dados. Todos os pacotes enviados ou recebidos em um soquete do tipo **Sock \_ RAW** são tratados como datagrams em um soquete não conectado.

As regras a seguir se aplicam às operações em soquetes **\_ brutos Sock** :

-   A função [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) ou [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) normalmente é usada para enviar dados em um soquete do tipo **Sock \_ RAW**. O endereço de destino pode ser qualquer endereço válido na família de endereços do soquete, incluindo um endereço de difusão ou multicast. Para enviar para um endereço de difusão, um aplicativo deve ter usado [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) com a \_ difusão habilitada. Caso contrário, **SendTo** ou **WSASendTo** falhará com o código de erro [WSAEACCES](windows-sockets-error-codes-2.md). Para IP, um aplicativo pode enviar para qualquer endereço de multicast (sem se tornar um membro do grupo).
-   Ao enviar dados IPv4, um aplicativo tem a opção de especificar o cabeçalho IPv4 na frente do datagrama de saída para o pacote. Se a opção **IP \_ HDRINCL** Socket estiver definida como true para um soquete IPv4 (família de endereços da \_ inet série AF), o aplicativo deverá fornecer o cabeçalho IPv4 nos dados de saída para operações de envio. Se essa opção de soquete for falsa (a configuração padrão), o cabeçalho IPv4 não deverá estar incluído nos dados de saída para operações de envio.
-   Ao enviar dados IPv6, um aplicativo tem a opção de especificar o cabeçalho IPv6 na frente do datagrama de saída para o pacote. Se a opção de soquete de **\_ HDRINCL IPv6** estiver definida como true para um soquete IPv6 (família de endereços de AF \_ INET6), o aplicativo deverá fornecer o cabeçalho IPv6 nos dados de saída para operações de envio. A configuração padrão para essa opção é false. Se essa opção de soquete for falsa (a configuração padrão), o cabeçalho IPv6 não deverá ser incluído nos dados de saída para operações de envio. Para IPv6, não deve haver necessidade de incluir o cabeçalho IPv6. Se as informações estiverem disponíveis usando funções de soquete, o cabeçalho IPv6 não deverá ser incluído para evitar problemas de compatibilidade no futuro. Esses problemas são discutidos no RFC 3542 publicado pela IETF. Usar a opção de soquete de **\_ HDRINCL IPv6** não é recomendado e pode ser preterido no futuro.
-   A função [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) ou [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) normalmente é usada para receber dados em um soquete do tipo **\_ RAW Sock**. Ambas as funções têm uma opção para retornar o endereço IP de origem do qual o pacote foi enviado. Os dados recebidos são um datagrama de um soquete não conectado.
-   Para IPv4 (família de endereços da inet da série AF \_ ), um aplicativo recebe o cabeçalho IP na frente de cada datagrama recebido, independentemente da opção de soquete **IP \_ HDRINCL** .
-   Para IPv6 (família de endereços de AF \_ INET6), um aplicativo recebe tudo após o último cabeçalho IPv6 em cada datagrama recebido, independentemente da opção de soquete **\_ HDRINCL do IPv6** . O aplicativo não recebe nenhum cabeçalho IPv6 usando um soquete bruto.
-   Os datagramas recebidos são copiados em todos os soquetes **\_ brutos do Sock** que atendem às seguintes condições:

    -   O número de protocolo especificado no parâmetro de *protocolo* quando o soquete foi criado deve corresponder ao número de protocolo no cabeçalho IP do datagrama recebido.
    -   Se um endereço IP local for definido para o soquete, ele deverá corresponder ao endereço de destino conforme especificado no cabeçalho IP do datagrama recebido. Um aplicativo pode especificar o endereço IP local chamando a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) . Se nenhum endereço IP local for especificado para o soquete, os datagrams serão copiados no soquete, independentemente do endereço IP de destino no cabeçalho IP do datagrama recebido.
    -   Se um endereço externo for definido para o soquete, ele deverá corresponder ao endereço de origem, conforme especificado no cabeçalho IP do datagrama recebido. Um aplicativo pode especificar o endereço IP externo chamando a função [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) . Se nenhum endereço IP externo for especificado para o soquete, os datagramas serão copiados no soquete, independentemente do endereço IP de origem no cabeçalho IP do datagrama recebido.

É importante entender que alguns soquetes do tipo **\_ RAW Sock** podem receber muitos datagramas inesperados. Por exemplo, um programa PING pode criar um soquete do tipo **Sock \_ RAW** para enviar solicitações de eco ICMP e receber respostas. Embora o aplicativo esteja esperando respostas de eco ICMP, todas as outras mensagens ICMP (como o HOST ICMP \_ inacessível) também podem ser entregues a esse aplicativo. Além disso, se vários soquetes **\_ brutos Sock** estiverem abertos em um computador ao mesmo tempo, os mesmos datagramas poderão ser entregues a todos os soquetes abertos. Um aplicativo deve ter um mecanismo para reconhecer os datagramas de interesse e ignorar todos os outros. Para um programa PING, tal mecanismo pode incluir inspecionar o cabeçalho IP recebido para identificadores exclusivos no cabeçalho ICMP (a ID do processo do aplicativo, por exemplo).

> [!Note]  
> Para usar um soquete do tipo **Sock \_ RAW** , é necessário ter privilégios administrativos. Os usuários que executam aplicativos Winsock que usam soquetes brutos devem ser membros do grupo Administradores no computador local, caso contrário, as chamadas de soquete brutas falharão com um código de erro de [WSAEACCES](windows-sockets-error-codes-2.md). No Windows Vista e posterior, o acesso a soquetes brutos é imposto na criação do soquete. Nas versões anteriores do Windows, o acesso a soquetes brutos é imposto durante outras operações de soquete.

 

## <a name="common-uses-of-raw-sockets"></a>Usos comuns de soquetes brutos

Um uso comum de soquetes brutos é a solução de problemas de aplicativos que precisam examinar pacotes IP e cabeçalhos em detalhes. Por exemplo, um soquete bruto pode ser usado com o \_ IOCTL sio RCVALL para permitir que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede. Para obter mais informações, consulte a referência do [**sio \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

## <a name="limitations-on-raw-sockets"></a>Limitações em soquetes brutos

No Windows 7, no Windows Vista, no Windows XP com Service Pack 2 (SP2) e no Windows XP com Service Pack 3 (SP3), a capacidade de enviar tráfego sobre soquetes brutos foi restrita de várias maneiras:

-   Os dados TCP não podem ser enviados por meio de soquetes brutos.
-   Os datagramas UDP com um endereço de origem inválido não podem ser enviados por meio de soquetes brutos. O endereço IP de origem para qualquer datagrama UDP de saída deve existir em uma interface de rede ou o datagrama é Descartado. Essa alteração foi feita para limitar a capacidade de código mal-intencionado de criar ataques de negação de serviço distribuídos e limita a capacidade de enviar pacotes falsificados (pacotes TCP/IP com um endereço IP de origem forjado).
-   Não é permitida uma chamada para a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) com um soquete bruto para o \_ protocolo TCP IPPROTO.
    > [!Note]  
    > A função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) com um soquete bruto é permitida para outros protocolos (IPPROTO \_ IP, IPPROTO \_ UDP ou IPPROTO \_ SCTP, por exemplo).

     

Essas restrições acima não se aplicam ao Windows Server 2008 R2, ao Windows Server 2008, ao Windows Server 2003 ou às versões do sistema operacional anteriores ao Windows XP com SP2.

> [!Note]  
> A implementação da Microsoft do TCP/IP no Windows é capaz de abrir um soquete UDP ou TCP bruto com base nas restrições acima. Outros provedores Winsock podem não dar suporte ao uso de soquetes brutos.

 

Há mais limitações para aplicativos que usam um soquete do tipo **Sock \_ RAW**. Por exemplo, todos os aplicativos que escutam um protocolo específico receberão todos os pacotes recebidos para esse protocolo. Isso pode não ser o que é desejado para vários aplicativos usando um protocolo. Isso também não é adequado para aplicativos de alto desempenho. Para resolver esses problemas, pode ser necessário gravar um driver de protocolo de rede do Windows (driver de dispositivo) para o protocolo de rede específico. No Windows Vista e posterior, o kernel do Winsock (WSK), uma nova interface de programação de rede de modo de kernel independente de transporte pode ser usada para gravar um driver de protocolo de rede. No Windows Server 2003 e versões anteriores, um provedor de interface do driver de transporte (TDI) e uma DLL auxiliar do Winsock podem ser escritos para dar suporte ao protocolo de rede. O protocolo de rede seria então adicionado ao catálogo do Winsock como um protocolo com suporte. Isso permite que vários aplicativos abram soquetes para esse protocolo específico e o driver de dispositivo possa manter o controle de qual soquete recebe erros e pacotes específicos. Para obter informações sobre como escrever um provedor de protocolo de rede, consulte as seções em WSK e TDI no Windows Driver Kit (WDK).

Os aplicativos também precisam estar cientes do impacto que as configurações de firewall podem ter ao enviar e receber pacotes usando soquetes brutos.

 

 
