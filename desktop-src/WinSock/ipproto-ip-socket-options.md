---
description: As tabelas a seguir descrevem \_ as opções de soquete de IP IPPROTO que se aplicam aos soquetes criados para a família de endereços IPv4 (INET série AF \_ ). Consulte as páginas de referência de função getsockopt e setsockopt para obter mais informações sobre como obter e definir opções de soquete.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: Opções de soquete IPPROTO_IP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: b4c8daa18e7bd60e61473bdda1c885bbd163f0b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764139"
---
# <a name="ipproto_ip-socket-options"></a>\_Opções de soquete de IP IPPROTO

As tabelas a seguir descrevem **IPPROTO_IP** opções de soquete que se aplicam aos soquetes criados para a família de endereços IPv4 (INET série AF \_ ). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Algumas opções de soquete exigem mais explicações do que essas tabelas podem ser transmitidas; essas opções contêm links para páginas adicionais.

## <a name="options"></a>Opções

| Opção | Obter | Definir | Tipo de optval | Descrição |
|-|-|-|-|-|
| IP_ADD_IFLIST | | sim | DWORD (IF_INDEX) | Adiciona um índice de interface ao IFLIST associado à opção **IP_IFLIST** . |
| IP_ADD_MEMBERSHIP | | sim | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Junte o soquete ao grupo de multicast fornecido na interface especificada. |
| IP_ADD_SOURCE_MEMBERSHIP | | sim | [**\_origem de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Ingresse no grupo de multicast fornecido na interface especificada e aceite dados provenientes do endereço de origem fornecido. |
| \_origem do bloco de IP \_ | | sim | [**\_origem de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Remove a origem fornecida como um remetente para o grupo e a interface multicast fornecidos. |
| IP_DEL_IFLIST | | sim | DWORD (IF_INDEX) | Remove um índice de interface do IFLIST associado à opção **IP_IFLIST** . As entradas podem ser removidas somente pelo aplicativo, portanto, lembre-se de que as entradas podem ficar obsoletas depois que uma interface é removida. |
| \_DONTFRAGMENT IP | sim | sim | DWORD (booliano) | Indica que os dados não devem ser fragmentados, independentemente da MTU local. Válido somente para protocolos orientados a mensagens. Os provedores de TCP/IP da Microsoft respeitam essa opção para UDP e ICMP. |
| \_Associação IP drop \_ | | sim | [**\_mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Deixa o grupo de multicast especificado da interface especificada. Os provedores de serviços devem oferecer suporte a essa opção quando houver suporte para multicast. O suporte é indicado na estrutura de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) retornada por uma chamada de função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) com o seguinte: xpi \_ support \_ MultiPoint = 1, XP1 \_ MultiPoint \_ Control \_ plano = 0, XP1 \_ MultiPoint \_ Data \_ plano = 0. |
| \_Associação de \_ origem IP drop \_ | | sim | [**\_origem de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Descarta a associação ao grupo de multicast, à interface e ao endereço de origem fornecidos. |
| IP_GET_IFLIST | sim | | DWORD [] (IF_INDEX []) | Obtém o IFLIST atual associado à opção **IP_IFLIST** . Retornará um erro se **IP_IFLIST** não estiver habilitado. |
| \_HDRINCL IP | sim | sim | DWORD (booliano) | Quando definido como **true**, indica que o aplicativo fornece o cabeçalho IP. Aplica-se somente a \_ soquetes brutos Sock. O provedor de serviços TCP/IP pode definir o campo ID, se o valor fornecido pelo aplicativo for zero.  A \_ opção IP HDRINCL é aplicada somente ao \_ tipo de protocolo bruto Sock. Um provedor de serviços TCP/IP que dá suporte ao SOCK \_ RAW também deve dar suporte a \_ HDRINCL IP.  |
| IP_IFLIST | sim | sim | DWORD (booliano) | Obtém ou define o estado de **IP_IFLIST** do soquete. Quando essa opção é definida como true, a recepção de datagrama é restrita a interfaces que estão no IFLIST. Os datagramas recebidos em outras interfaces são ignorados. IFLIST começa vazio. Use **IP_ADD_IFLIST** e **IP_DEL_IFLIST** para editar o IFLIST. |
| MTU de IP \_ | sim | | DWORD | Obtém a estimativa do sistema da MTU do caminho. O soquete deve estar conectado. |
| \_descoberta de MTU de IP \_ | sim | sim | DWORD (**\_ estado do PMTUD**) | Obtém ou define o estado de descoberta de MTU do caminho para o soquete. O valor padrão é **IP \_ PMTUDISC \_ não \_ definido**. Para soquetes de fluxo, **\_ PMTUDISC IP \_ não \_ definido** e o **IP \_ PMTUDISC \_** executará a descoberta de MTU de caminho. **IP \_ PMTUDISC \_** não e **a \_ \_ investigação de PMTUDISC de IP** DESligará a descoberta de MTU de caminho. Para soquetes de datagramas, o **IP \_ PMTUDISC \_** forçará todos os pacotes de saída a ter o bit DF definido e uma tentativa de enviar pacotes maiores que o Path MTU resultará em um erro. **IP \_ PMTUDISC \_** não forçará todos os pacotes de saída a ter o bit DF não definido, e os pacotes serão fragmentados de acordo com a interface MTU. **IP \_ A \_ investigação PMTUDISC** forçará todos os pacotes de saída a ter o bit DF definido, e uma tentativa de enviar pacotes maiores do que a interface MTU resultará em um erro. |
| IP \_ multicast \_ se | sim | sim | DWORD | Obtém ou define a interface de saída para enviar o tráfego de multicast IPv4. Essa opção não altera a interface padrão para receber o tráfego multicast IPv4.  O valor de entrada para definir essa opção é um endereço IPv4 de 4 bytes na ordem de bytes de rede. Esse parâmetro DWORD também pode ser um índice de interface em ordem de bytes de rede. Qualquer endereço IP no bloco 0. x. x. x (primeiro octeto de 0), exceto o endereço IPv4 0.0.0.0, é tratado como um índice de interface. Um índice de interface é um número de 24 bits e o bloco de endereço IPv4 0.0.0.0/8 não é usado (esse intervalo é reservado). O índice de interface pode ser usado para especificar a interface padrão para o tráfego multicast para IPv4. Se *optval* for zero, a interface padrão para receber multicast será especificada para o envio de tráfego multicast.  Ao obter essa opção, o *optval* retorna o índice de interface padrão atual para enviar o tráfego IPv4 multicast na ordem de bytes do host. |
| \_loop multicast de IP \_ | sim | sim | DWORD (booliano) | Controla se os dados enviados por um aplicativo no computador local (não necessariamente pelo mesmo soquete) em uma sessão de multicast serão recebidos por um soquete ingressado no grupo de destino de multicast na interface de loopback. Um valor **true** faz com que os dados multicast enviados por um aplicativo no computador local sejam entregues a um soquete de escuta na interface de loopback. Um valor **false** impede que os dados multicast enviados por um aplicativo no computador local sejam entregues a um soquete de escuta na interface de loopback. Por padrão, **o \_ \_ loopback multicast IP** está habilitado. |
| \_TTL de multicast IP \_ | sim | sim | DWORD | Define/Obtém o valor de TTL associado ao tráfego de multicast de IP no soquete. |
| opções de IP \_ | sim | sim | º \[\] | Especifica as opções de IP a serem inseridas em pacotes de saída. A configuração de novas opções substitui todas as opções especificadas anteriormente. A definição de optval como zero remove todas as opções especificadas anteriormente. O \_ suporte às opções de IP não é necessário; para verificar se \_ as opções de IP têm suporte, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obter as opções atuais. Se **getsockopt** falhar, \_ não haverá suporte para as opções de IP. |
| chegada de IP \_ original \_ \_ se | sim | sim | DWORD (booliano) | Indica se a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve retornar dados de controle opcionais contendo a interface de entrada onde o pacote foi recebido para soquetes de datagrama. Essa opção permite que a interface IPv4 em que o pacote foi recebido seja retornada na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Essa opção só é válida em soquetes de datagrama e brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| [\_PKTINFO IP](ip-pktinfo.md) | sim | sim | DWORD | Indica que as informações de pacote devem ser retornadas pela função **WSARecvMsg** . |
| \_difusão de recebimento de IP \_ | sim | sim | DWORD (booliano) | Permite ou bloqueia a recepção de difusão. |
| \_RECVIF IP | sim | sim | DWORD (booliano) | Indica se a pilha de IP deve preencher o buffer de controle com detalhes sobre qual interface recebeu um pacote com um soquete de datagrama. Quando esse valor for true, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retornará dados de controle opcionais contendo a interface em que o pacote foi recebido para soquetes de datagrama. Essa opção permite que a interface IPv4 em que o pacote foi recebido seja retornada na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Essa opção só é válida em soquetes de datagrama e brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| \_RECVTOS IP | sim | sim | DWORD (booliano) | Indica se a pilha de IP deve preencher o buffer de controle com uma mensagem que contém o campo de cabeçalho IPv4 TOS (tipo de serviço) em um datagrama recebido. Quando esse valor for true, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retornará dados de controle opcionais contendo o valor do campo de cabeçalho IPv4 do tos do datagrama recebido.  Essa opção permite que o campo de cabeçalho IPv4 do TOS do datagrama recebido seja retornado na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . O tipo de mensagem retornado será IP \_ tos. Todos os bits DSCP e ECN do campo TOS serão retornados.  Essa opção só é válida em soquetes de datagrama (o tipo de soquete deve ser SOCK \_ DGRAM).  |
| \_RECVTTL IP | sim | sim | DWORD (booliano) | Indica que as informações de salto (TTL) devem ser retornadas na função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Se *optval* for definido como **1** na chamada para [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), a opção será habilitada. Se definido como **0**, a opção será desabilitada.  Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| TOS de IP \_ | sim | sim | DWORD (booliano) | Não use. As configurações do tipo de serviço (TOS) só devem ser definidas usando a qualidade da API de serviço. Consulte [serviços diferenciados](/previous-versions/windows/desktop/qos/differentiated-services) na seção qualidade de serviço do SDK da plataforma para obter mais informações. |
| TTL de IP \_ | sim | sim | DWORD (booliano) | Altera o valor padrão definido pelo provedor de serviços TCP/IP no campo TTL do cabeçalho IP em datagramas de saída. O \_ suporte a TTL de IP não é necessário; para verificar se o TTL de IP tem \_ suporte, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obter as opções atuais. Se **getsockopt** falhar, o \_ TTL de IP não terá suporte. |
| \_origem de desbloqueio de IP \_ | | sim | [**\_origem de mreq IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Adiciona a origem fornecida como um remetente ao grupo e à interface multicast fornecidos. |
| IP \_ unicast \_ se | sim | sim | DWORD (se \_ índice) | Obtém ou define a interface de saída para enviar tráfego IPv4. Essa opção não altera a interface padrão para receber o tráfego IPv4. Essa opção é importante para computadores de hospedagem múltipla.  O valor de entrada para definir essa opção é um endereço IPv4 de 4 bytes na ordem de bytes de rede. Esse parâmetro DWORD deve ser um índice de interface na ordem de bytes de rede. Qualquer endereço IP no bloco 0. x. x. x (primeiro octeto de 0), exceto o endereço IPv4 0.0.0.0, é tratado como um índice de interface. Um índice de interface é um número de 24 bits e o bloco de endereço IPv4 0.0.0.0/8 não é usado (esse intervalo é reservado). O índice de interface pode ser usado para especificar a interface padrão para o envio de tráfego para IPv4. A função [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) pode ser usada para obter as informações de índice da interface. Se *optval* for zero, a interface padrão para enviar tráfego será definida como não especificado.  Ao obter essa opção, o *optval* retorna o índice de interface padrão atual para enviar o tráfego IPv4 na ordem de bytes do host. |
| IP_USER_MTU | sim | sim | DWORD | Obtém ou define um limite superior no MTU da camada de IP (em bytes) para o soquete especificado. Se o valor for maior do que a estimativa do sistema do MTU do caminho (que você pode recuperar em um Soquete conectado consultando a opção de soquete **IP_MTU** ), a opção não terá nenhum efeito. Se o valor for inferior, os pacotes de saída maiores que isso serão fragmentados ou não serão enviados, dependendo do valor de **IP_DONTFRAGMENT**. O valor padrão é **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para a segurança de tipo, você deve usar as funções [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) em vez de usar a opção socket diretamente. |
| \_contexto de \_ redirecionamento WFP de IP \_ | sim | sim | WSACMSGHDR com dados de controle | Um tipo de dados auxiliar de soquete de datagrama ( \_ tipo CMsg) para indicar o contexto de redirecionamento para um soquete UDP usado por um serviço de redirecionamento WFP (Windows Filtering Platform) de modo de usuário. |
| \_registros de \_ redirecionamento de WFP de IP \_ | sim | sim | WSACMSGHDR com dados de controle | Um tipo de dados auxiliar de soquete de datagrama ( \_ tipo CMsg) para indicar o registro de redirecionamento para um soquete UDP usado por um serviço de redirecionamento WFP (Windows Filtering Platform) de modo de usuário. |

## <a name="windows-support-for-ip_proto-options"></a>Suporte do Windows para \_ Opções de IP proto

| Opção | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | A partir do Windows 10, versão 1803 | | | | | |
| \_Adicionar \_ Associação de IP | x | x | x | x | x | x |
| IP \_ Adicionar \_ Associação de origem \_ | x | x | x | x | x | x |
| \_origem do bloco de IP \_ | x | x | x | x | x | x |
| IP_DEL_IFLIST | A partir do Windows 10, versão 1803 | | | | | |
| \_DONTFRAGMENT IP | x | x | x | x | x | x |
| \_Associação IP drop \_ | x | x | x | x | x | x |
| \_Associação de \_ origem IP drop \_ | x | x | x | x | x | x |
| IP_GET_IFLIST | A partir do Windows 10, versão 1803 | | | | | |
| \_HDRINCL IP | x | x | x | x | x | x |
| IP_IFLIST | A partir do Windows 10, versão 1803 | | | | | |
| IP \_ multicast \_ se | x | x | x | x | x | x |
| \_loop multicast de IP \_ | x | x | x | x | x | x |
| \_TTL de multicast IP \_ | x | x | x | x | x | x |
| opções de IP \_ | x | x | x | x | x | x |
| chegada de IP \_ original \_ \_ se | x | x | x | x | | |
| \_PKTINFO IP | x | x | x | x | x | x |
| \_difusão de recebimento de IP \_ | x | x | x | x | x | x |
| \_RECVIF IP | A partir do Windows 10, versão 1703 | x | x | x | x | x |
| \_RECVTTL IP | x | | | | | |
| TOS de IP \_ | x | x | x | | | |
| TTL de IP \_ | x | x | x | x | x | x |
| \_origem de desbloqueio de IP \_ | x | x | x | x | x | x |
| IP \_ unicast \_ se | x | x | x | x | x | x |
| \_contexto de \_ redirecionamento WFP de IP \_ | x | x | x | | | |
| \_registros de \_ redirecionamento de WFP de IP \_ | x | x | x | | | |

<br/>

| Opção | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| \_Adicionar \_ Associação de IP | x | x |
| IP \_ Adicionar \_ Associação de origem \_ | x | x |
| \_origem do bloco de IP \_ | x | x |
| IP_DEL_IFLIST | | |
| \_DONTFRAGMENT IP | x | x |
| \_Associação IP drop \_ | x | x |
| \_Associação de \_ origem IP drop \_ | x | x |
| IP_GET_IFLIST | | |
| \_HDRINCL IP | x | x |
| IP_IFLIST | | |
| IP \_ multicast \_ se | x | x |
| \_loop multicast de IP \_ | x | x |
| \_TTL de multicast IP \_ | x | x |
| opções de IP \_ | x | x |
| chegada de IP \_ original \_ \_ se | | |
| \_PKTINFO IP | x | x |
| \_difusão de recebimento de IP \_ | x | x |
| \_RECVIF IP | | |
| \_RECVTTL IP | | |
| TOS de IP \_ | | |
| TTL de IP \_ | x | x |
| \_origem de desbloqueio de IP \_ | x | x |
| IP \_ unicast \_ se | | |
| \_contexto de \_ redirecionamento WFP de IP \_ | | |
| \_registros de \_ redirecionamento de WFP de IP \_ | | |

## <a name="remarks"></a>Comentários

No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o nível de **\_ IP IPPROTO** é definido no arquivo de cabeçalho *Ws2def. h* , que é incluído automaticamente no arquivo de cabeçalho *Winsock2. h* . Algumas das opções de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Ws2ipdef. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Ws2tcpip. h* . As opções restantes de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Wsipv6ok. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* . Os arquivos de cabeçalho *Ws2def. h*, *Ws2ipdef. h* e *Wsipv6ok. h* nunca devem ser usados diretamente.

No SDK da plataforma lançado para o Windows Server 2003 e Windows XP, o nível de **\_ IP IPPROTO** é definido no arquivo de cabeçalho *Winsock2. h* . Algumas das opções de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Ws2tcpip. h* . As opções restantes de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Wsipv6ok. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* . O arquivo de cabeçalho *Wsipv6ok. h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | <dl> <dt>Ws2def. h (incluir Winsock2. h); </dt> <dt>Ws2ipdef. h (incluir Ws2tcpip. h); </dt> <dt>Wsipv6ok. h (incluir Winsock2. h)</dt> </dl> |
