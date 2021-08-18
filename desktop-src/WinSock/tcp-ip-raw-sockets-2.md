---
description: Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente.
ms.assetid: 4cbe5505-75e7-454f-9e6b-f38bdc60bf6d
title: Soquetes brutos TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef8600c7b1a6c1bc5b2f7b5b210ca2d56f90069b0afce88c83ca45e9cfad8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733386"
---
# <a name="tcpip-raw-sockets"></a>Soquetes brutos TCP/IP

Um soquete bruto é um tipo de soquete que permite o acesso ao provedor de transporte subjacente. Este tópico se concentra apenas em soquetes brutos e nos protocolos IPv4 e IPv6. Isso porque a maioria dos outros protocolos com exceção do ATM não é suportada por soquetes brutos. Para usar soquetes brutos, um aplicativo precisa ter informações detalhadas sobre o protocolo subjacente que está sendo usado.

Os provedores de serviços Winsock para o protocolo IP podem dar suporte a um tipo *de soquete* **SOCK \_ RAW.** O provedor Windows Sockets 2 para TCP/IP incluído no Windows dá suporte a esse tipo de soquete **SOCK \_** RAW.

Há dois tipos básicos desses soquetes brutos:

-   O primeiro tipo usa um tipo de protocolo conhecido escrito no título IP reconhecido por um provedor de serviços Winsock. Um exemplo do primeiro tipo de soquete é um soquete para o protocolo ICMP (tipo de protocolo IP = 1) ou o protocolo ICMPv6 (tipo procotol IP = 58).
-   O segundo tipo permite que qualquer tipo de protocolo seja especificado. Um exemplo do segundo tipo seria um protocolo experimental que não tem suporte direto do provedor de serviços Winsock, como o PROTOCOLO SCTP.

## <a name="determining-if-raw-sockets-are-supported"></a>Determinando se há suporte para soquetes brutos

Se um provedor de serviços Winsock dá suporte a soquetes **SOCK \_ RAW** para as famílias de endereços AF INET ou AF INET6, o tipo de soquete DE SOCK RAW deve ser incluído na estrutura \_ INFO \_ [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) retornada pela [**função WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) **\_** para um ou mais dos provedores de transporte disponíveis.

O membro **iAddressFamily** na estrutura [**INFO \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) deve especificar AF INET ou AF INET6 e o membro \_ \_ **iSocketType** da estrutura **INFO WSAPROTOCOL \_** deve especificar SOCK **\_ RAW** para um dos provedores de transporte.

O **membro iProtocol** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pode ser definido como **\_ IP IPROTO.** O membro **iProtocol** da estrutura **INFO \_ WSAPROTOCOL** também poderá ser definido como zero se o provedor de serviços permitir que um aplicativo use um tipo de soquete **SOCK \_ RAW** para outros protocolos de rede que não sejam o Protocolo da Internet para a família de endereços.

Os outros membros na estrutura [**INFO \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) indicam outras propriedades do suporte de protocolo para **SOCK \_ RAW** e indicam como um soquete **de SOCK \_ RAW** deve ser tratado. Esses outros membros das INFORMAÇÕES **WSAPROTOCOL \_** para **SOCK \_ RAW** normalmente especificam que o protocolo é sem conexão, orientado a mensagens, dá suporte a difusão/multicast (os bits XP1 CONNECTIONLESS, XP1 MESSAGE ORIENTED, XP1 SUPPORT BROADCAST e XP1 SUPPORT MULTIPOINT são definidos no membro dwServiceFlags1) e podem ter um tamanho máximo de mensagem de \_ \_ \_ \_ \_ \_ \_ 65.467 bytes.

No Windows XP e posterior, o *comandoNetSh.exe* pode ser usado para determinar se há suporte para soquetes brutos. O comando a seguir executado em uma janela do CMD exibirá dados do catálogo winsock no console:

**netsh winsock show catalog**

A saída incluirá uma lista que contém alguns dos dados das estruturas [**de INFORMAÇÕES \_ WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) com suporte no computador local. Pesquise o termo RAW/IP ou RAW/IPv6 no campo Descrição para encontrar os protocolos que suportam soquetes brutos.

## <a name="creating-a-raw-socket"></a>Criando um soquete bruto

Para criar um soquete do [](/windows/desktop/api/Winsock2/nf-winsock2-socket) tipo **SOCK \_ RAW**, chame o soquete ou a função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) com o parâmetro *af* (família de endereços) definido como AF INET ou \_ AF \_ INET6,   o parâmetro de tipo definido como **SOCK \_ RAW** e o parâmetro de protocolo definido como o número de protocolo necessário. O *parâmetro* de protocolo se torna o valor do protocolo no header IP (SCTP é 132, por exemplo).

> [!Note]  
> Um aplicativo pode não especificar zero  (0) como o parâmetro de protocolo para as funções [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket), [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)e [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) se o parâmetro *de* tipo estiver definido como **SOCK \_ RAW.**

 

Soquetes brutos oferecem a capacidade de manipular o transporte subjacente, para que possam ser usados para fins mal-intencionados que representam uma ameaça à segurança. Portanto, somente os membros do grupo Administradores podem criar soquetes do tipo SOCK \_ RAW Windows 2000 e posterior.

## <a name="send-and-receive-operations"></a>Operações de envio e recebimento

Depois que um aplicativo cria um soquete do tipo **SOCK \_ RAW,** esse soquete pode ser usado para enviar e receber dados. Todos os pacotes enviados ou recebidos em um soquete do tipo **SOCK \_ RAW** são tratados como datagramas em um soquete não conectado.

As seguintes regras se aplicam às operações em **soquetes SOCK \_ RAW:**

-   A [**função sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) [**ou WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) normalmente é usada para enviar dados em um soquete do tipo **SOCK \_ RAW.** O endereço de destino pode ser qualquer endereço válido na família de endereços do soquete, incluindo um endereço de difusão ou multicast. Para enviar para um endereço de difusão, um aplicativo deve ter usado [**setsockopt com**](/windows/desktop/api/winsock/nf-winsock-setsockopt) SO \_ BROADCAST habilitado. Caso contrário, **sendto** **ou WSASendTo** falhará com o código de erro [WSAEACCES](windows-sockets-error-codes-2.md). Para IP, um aplicativo pode enviar para qualquer endereço multicast (sem se tornar um membro do grupo).
-   Ao enviar dados IPv4, um aplicativo tem a opção de especificar o header IPv4 na frente do datagrama de saída para o pacote. Se a opção de soquete **\_ IP HDRINCL** estiver definida como true para um soquete IPv4 (família de endereços de AF INET), o aplicativo deverá fornecer o header IPv4 nos dados de saída para operações de \_ envio. Se essa opção de soquete for false (a configuração padrão), o header IPv4 não deverá estar incluído nos dados de saída para operações de envio.
-   Ao enviar dados IPv6, um aplicativo tem a opção de especificar o header IPv6 na frente do datagrama de saída para o pacote. Se a opção de **soquete \_ HDRINCL IPV6** estiver definida como true para um soquete IPv6 (família de endereços de AF INET6), o aplicativo deverá fornecer o \_ header IPv6 nos dados de saída para operações de envio. A configuração padrão para essa opção é false. Se essa opção de soquete for false (a configuração padrão), o header IPv6 não deverá ser incluído nos dados de saída para operações de envio. Para IPv6, não deve haver necessidade de incluir o header IPv6. Se as informações estão disponíveis usando funções de soquete, o header IPv6 não deve ser incluído para evitar problemas de compatibilidade no futuro. Esses problemas são discutidos na RFC 3542 publicada pelo IETF. Usar a **opção de soquete \_ HDRINCL IPV6** não é recomendado e pode ser preterido no futuro.
-   A [**função recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) [**ou WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) normalmente é usada para receber dados em um soquete do tipo **SOCK \_ RAW.** Ambas as funções têm uma opção para retornar o endereço IP de origem do qual o pacote foi enviado. Os dados recebidos são um datagrama de um soquete não conectado.
-   Para IPv4 (família de endereços de AF INET), um aplicativo recebe o header IP na frente de cada datagrama recebido, independentemente da opção de soquete \_ **IP \_ HDRINCL.**
-   Para IPv6 (família de endereços de AF INET6), um aplicativo recebe tudo após o último header IPv6 em cada datagrama recebido, independentemente da opção de soquete \_ **\_ HDRINCL IPV6.** O aplicativo não recebe nenhum headers IPv6 usando um soquete bruto.
-   Os datagramas recebidos são copiados em todos os soquetes **SOCK \_ RAW** que atendem às seguintes condições:

    -   O número de protocolo especificado no parâmetro *de* protocolo quando o soquete foi criado deve corresponder ao número de protocolo no header IP do datagrama recebido.
    -   Se um endereço IP local for definido para o soquete, ele deverá corresponder ao endereço de destino, conforme especificado no header IP do datagrama recebido. Um aplicativo pode especificar o endereço IP local chamando a [**função bind.**](/windows/desktop/api/winsock/nf-winsock-bind) Se nenhum endereço IP local for especificado para o soquete, os datagramas serão copiados para o soquete, independentemente do endereço IP de destino no header IP do datagrama recebido.
    -   Se um endereço externo for definido para o soquete, ele deverá corresponder ao endereço de origem, conforme especificado no header IP do datagrama recebido. Um aplicativo pode especificar o endereço IP externo chamando [**a função connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) ou [**WSAConnect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect) Se nenhum endereço IP externo for especificado para o soquete, os datagramas serão copiados para o soquete, independentemente do endereço IP de origem no header IP do datagrama recebido.

É importante entender que alguns soquetes do tipo **SOCK \_ RAW** podem receber muitos datagramas inesperados. Por exemplo, um programa PING pode criar um soquete do tipo **SOCK \_ RAW** para enviar solicitações de eco ICMP e receber respostas. Enquanto o aplicativo está esperando respostas de eco ICMP, todas as outras mensagens ICMP (como HOST ICMP INACESSÍVEL) também podem ser entregues \_ a esse aplicativo. Além disso, se vários soquetes **SOCK \_ RAW** estão abertos em um computador ao mesmo tempo, os mesmos datagramas podem ser entregues a todos os soquetes abertos. Um aplicativo deve ter um mecanismo para reconhecer os datagramas de interesse e ignorar todos os outros. Para um programa PING, esse mecanismo pode incluir a inspeção do header IP recebido para identificadores exclusivos no header ICMP (a ID do processo do aplicativo, por exemplo).

> [!Note]  
> Usar um soquete do tipo **SOCK \_ RAW** requer privilégios administrativos. Os usuários que executam aplicativos Winsock que usam soquetes brutos devem ser membros do grupo Administradores no computador local; caso contrário, as chamadas de soquete bruto falharão com um código de erro [WSAEACCES](windows-sockets-error-codes-2.md). No Windows Vista e posterior, o acesso para soquetes brutos é imposto na criação do soquete. Em versões anteriores do Windows, o acesso para soquetes brutos é imposto durante outras operações de soquete.

 

## <a name="common-uses-of-raw-sockets"></a>Usos comuns de soquetes brutos

Um uso comum de soquetes brutos são a solução de problemas de aplicativos que precisam examinar os pacotes IP e os headers em detalhes. Por exemplo, um soquete bruto pode ser usado com o IOCTL SIO RCVP para permitir que um soquete receba todos os pacotes IPv4 ou IPv6 que passam por um \_ adaptador de rede. Para obter mais informações, consulte a [**referência do SIO \_ RC LTD.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

## <a name="limitations-on-raw-sockets"></a>Limitações em soquetes brutos

No Windows 7, Windows Vista, Windows XP com Service Pack 2 (SP2) e Windows XP com Service Pack 3 (SP3), a capacidade de enviar tráfego por soquetes brutos foi restrita de várias maneiras:

-   Os dados TCP não podem ser enviados por soquetes brutos.
-   Datagramas UDP com um endereço de origem inválido não podem ser enviados por soquetes brutos. O endereço de origem IP para qualquer datagrama UDP de saída deve existir em um interface de rede ou o datagrama é descartado. Essa alteração foi feita para limitar a capacidade de código mal-intencionado de criar ataques de negação de serviço distribuídos e limita a capacidade de enviar pacotes falsos (pacotes TCP/IP com um endereço IP de origem forjado).
-   Uma chamada para a [**função bind**](/windows/desktop/api/winsock/nf-winsock-bind) com um soquete bruto para o protocolo TCP IPPROTO não \_ é permitida.
    > [!Note]  
    > A [**função bind**](/windows/desktop/api/winsock/nf-winsock-bind) com um soquete bruto é permitida para outros protocolos (IP IPPROTO, \_ IPPROTO UDP ou \_ IPPROTO \_ SCTP, por exemplo).

     

Essas restrições acima não se aplicam ao Windows Server 2008 R2, Windows Server 2008 , Windows Server 2003 ou a versões do sistema operacional anteriores ao Windows XP com SP2.

> [!Note]  
> A implementação da Microsoft de TCP/IP no Windows é capaz de abrir um soquete UDP ou TCP bruto com base nas restrições acima. Outros provedores Winsock podem não dar suporte ao uso de soquetes brutos.

 

Há outras limitações para aplicativos que usam um soquete do tipo **SOCK \_ RAW.** Por exemplo, todos os aplicativos que escutam um protocolo específico receberão todos os pacotes recebidos para esse protocolo. Isso pode não ser o que é desejado para vários aplicativos usando um protocolo. Isso também não é adequado para aplicativos de alto desempenho. Para resolver esses problemas, pode ser necessário escrever um driver Windows de protocolo de rede (driver de dispositivo) para o protocolo de rede específico. No Windows Vista e posterior, o WSK (Winsock Kernel), um novo modo de programação de rede do modo kernel independente de transporte pode ser usado para escrever um driver de protocolo de rede. No Windows Server 2003 e anteriores, um provedor TDI (interface do driver de transporte) e uma DLL auxiliar winsock podem ser gravados para dar suporte ao protocolo de rede. Em seguida, o protocolo de rede seria adicionado ao catálogo winsock como um protocolo com suporte. Isso permite que vários aplicativos abram soquetes para esse protocolo específico e o driver de dispositivo possa controlar qual soquete recebe pacotes e erros específicos. para obter informações sobre como escrever um provedor de protocolo de rede, consulte as seções em WSK e TDI no Kit de Driver de Windows (WDK).

Os aplicativos também precisam estar cientes do impacto que as configurações de firewall podem ter ao enviar e receber pacotes usando soquetes brutos.

 

 
