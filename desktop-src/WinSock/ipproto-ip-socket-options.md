---
description: As tabelas a seguir descrevem as opções de soquete IP IPPROTO que se aplicam a soquetes criados para a família de \_ endereços IPv4 (AF \_ INET). Consulte as páginas de referência da função getsockopt e setsockopt para obter mais informações sobre como obter e definir opções de soquete.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: Opções de soquete IPPROTO_IP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 4ce469ab9989bc1cd3ec261e3d3a1b3b819c30443225fee24ae06c92efb6bace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927706"
---
# <a name="ipproto_ip-socket-options"></a>Opções de soquete \_ IP IPPROTO

As tabelas a seguir **descrevem IPPROTO_IP** de soquete que se aplicam a soquetes criados para a família de endereços IPv4 (AF \_ INET). Consulte as páginas de referência da função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Algumas opções de soquete exigem mais explicação do que essas tabelas podem transmitir; essas opções contêm links para páginas adicionais.

## <a name="options"></a>Opções

| Opção | Obter | Definir | Tipo de aceitação | Descrição |
|-|-|-|-|-|
| IP_ADD_IFLIST | | sim | DWORD (IF_INDEX) | Adiciona um índice de interface ao IFLIST associado à **IP_IFLIST** de interface. |
| IP_ADD_MEMBERSHIP | | sim | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Unir o soquete ao grupo de multicast fornecido na interface especificada. |
| IP_ADD_SOURCE_MEMBERSHIP | | sim | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Insere o grupo de multicast fornecido na interface fornecida e aceite os dados fornecidos do endereço de origem fornecido. |
| IP \_ BLOCK \_ SOURCE | | sim | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Remove a fonte fornecida como um remetente para o grupo e a interface multicast fornecidos. |
| IP_DEL_IFLIST | | sim | DWORD (IF_INDEX) | Remove um índice de interface do IFLIST associado à **IP_IFLIST** opção. As entradas podem ser removidas somente pelo aplicativo, portanto, esteja ciente de que as entradas podem ficar desa stale depois que uma interface é removida. |
| IP \_ DONTFRAGMENT | sim | sim | DWORD (booliana) | Indica que os dados não devem ser fragmentados independentemente da MTU local. Válido somente para protocolos orientados a mensagens. Os provedores TCP/IP da Microsoft respeitam essa opção para UDP e ICMP. |
| ASSOCIAÇÃO \_ AO IP DROP \_ | | sim | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Deixa o grupo de multicast especificado da interface especificada. Os provedores de serviços devem dar suporte a essa opção quando há suporte para multicast. O suporte é indicado na estrutura [**INFO WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) retornada por uma chamada de função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) com o seguinte: XPI \_ SUPPORT \_ MULTIPOINT=1, XP1 \_ MULTIPOINT CONTROL \_ \_ PLANE=0, XP1 \_ MULTIPOINT DATA \_ \_ PLANE=0. |
| ASSOCIAÇÃO \_ DE \_ ORIGEM DO IP DROP \_ | | sim | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Descarta a associação ao grupo multicast, à interface e ao endereço de origem determinados. |
| IP_GET_IFLIST | sim | | DWORD[] (IF_INDEX[]) | Obtém o IFLIST atual associado à **IP_IFLIST** atual. Retornará o erro **IP_IFLIST** não estiver habilitado. |
| IP \_ HDRINCL | sim | sim | DWORD (booliana) | Quando definido como **TRUE**, indica que o aplicativo fornece o header IP. Aplica-se somente a soquetes SOCK \_ RAW. O provedor de serviços TCP/IP poderá definir o campo ID, se o valor fornecido pelo aplicativo for zero.  A opção \_ IP HDRINCL é aplicada somente ao tipo DE PROTOCOLO SOCK \_ RAW. Um provedor de serviços TCP/IP que dá suporte a SOCK \_ RAW também deve dar suporte ao IP \_ HDRINCL.  |
| IP_IFLIST | sim | sim | DWORD (booliana) | Obtém ou define **o IP_IFLIST** do soquete. Quando essa opção é definida como true, a recepção de datagrama é restrita a interfaces que estão no IFLIST. Os datagramas recebidos em qualquer outra interface são ignorados. IFLIST inicia vazio. Use **IP_ADD_IFLIST** e **IP_DEL_IFLIST** editar o IFLIST. |
| IP \_ MTU | sim | | DWORD | Obtém a estimativa do sistema do caminho MTU. O soquete deve estar conectado. |
| IP \_ MTU \_ DISCOVER | sim | sim | DWORD (**ESTADO PMTUD \_**) | Obtém ou define o estado de descoberta de MTU do caminho para o soquete. O valor padrão é **IP \_ PMTUDISC \_ NOT \_ SET.** Para soquetes de fluxo, **IP \_ PMTUDISC \_ NOT \_ SET** e **IP \_ PMTUDISC \_ DO** executarão a descoberta de MTU de caminho. **IP \_ PMTUDISC \_ DONT e** IP **\_ PMTUDISC \_ PROBE** desativarão a descoberta de MTU de caminho. Para soquetes de datagrama, **o IP \_ PMTUDISC \_ DO** força todos os pacotes de saída a ter o bit DF definido e uma tentativa de enviar pacotes maiores que o caminho MTU resultará em um erro. **IP \_ PMTUDISC \_ DONT força** todos os pacotes de saída a não definirem o bit DF e os pacotes serão fragmentados de acordo com a interface MTU. **IP \_ PMTUDISC \_ PROBE** força todos os pacotes de saída a ter o bit DF definido, e uma tentativa de enviar pacotes maiores que a interface MTU resultará em um erro. |
| IP \_ MULTICAST \_ IF | sim | sim | DWORD | Obtém ou define a interface de saída para enviar o tráfego de multicast IPv4. Essa opção não altera a interface padrão para receber o tráfego de multicast IPv4.  O valor de entrada para definir essa opção é um endereço IPv4 de 4 byte na ordem de byte de rede. Esse parâmetro DWORD também pode ser um índice de interface na ordem de byte de rede. Qualquer endereço IP no bloco 0.x.x.x (primeiro octeto de 0), exceto o endereço IPv4 0.0.0.0, é tratado como um índice de interface. Um índice de interface é um número de 24 bits e o bloco de endereço IPv4 0.0.0.0/8 não é usado (esse intervalo é reservado). O índice de interface pode ser usado para especificar a interface padrão para o tráfego multicast para IPv4. Se *optval* for zero , a interface padrão para receber multicast será especificada para enviar o tráfego multicast.  Ao obter essa opção, a *aceitação* retorna o índice de interface padrão atual para enviar o tráfego IPv4 multicast na ordem de byte do host. |
| LOOP \_ MULTICAST \_ DE IP | sim | sim | DWORD (booliana) | Controla se os dados enviados por um aplicativo no computador local (não necessariamente pelo mesmo soquete) em uma sessão multicast serão recebidos por um soquete ingressado no grupo de destino multicast na interface de loopback. Um valor true **faz com** que os dados multicast enviados por um aplicativo no computador local sejam entregues a um soquete de escuta na interface de loopback. Um valor false **impede** que os dados multicast enviados por um aplicativo no computador local seja entregue a um soquete de escuta na interface de loopback. Por padrão, **o IP \_ MULTICAST \_ LOOPBACK** está habilitado. |
| IP \_ MULTICAST \_ TTL | sim | sim | DWORD | Define/obtém o valor de TTL associado ao tráfego de multicast IP no soquete. |
| OPÇÕES DE \_ IP | sim | sim | Char \[\] | Especifica as opções de IP a serem inseridas em pacotes de saída. Definir novas opções substitui todas as opções especificadas anteriormente. Definir optval como zero remove todas as opções especificadas anteriormente. O suporte a OPÇÕES de IP não é necessário; para verificar se há suporte para OPÇÕES DE \_ \_ IP, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obter as opções atuais. Se **getsockopt** falhar, não há suporte para IP \_ OPTIONS. |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | sim | sim | DWORD (booliana) | Indica se [**a função LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve retornar dados de controle opcionais que contêm a interface de chegada em que o pacote foi recebido para soquetes de datagrama. Essa opção permite que a interface IPv4 em que o pacote foi recebido seja retornado na estrutura [**WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Essa opção só é válida em datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou SOCK \_ RAW). |
| [IP \_ PKTINFO](ip-pktinfo.md) | sim | sim | DWORD | Indica que as informações de pacote devem ser retornadas pela **função WSARecvMsg.** |
| DIFUSÃO \_ DE RECEBIMENTO \_ DE IP | sim | sim | DWORD (booliana) | Permite ou bloqueia a recepção de difusão. |
| IP \_ RECVIF | sim | sim | DWORD (booliana) | Indica se a pilha IP deve preencher o buffer de controle com detalhes sobre qual interface recebeu um pacote com um soquete de datagrama. Quando esse valor for true, [**a função LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retornará dados de controle opcionais que contêm a interface em que o pacote foi recebido para soquetes de datagrama. Essa opção permite que a interface IPv4 em que o pacote foi recebido seja retornado na estrutura [**WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Essa opção só é válida em datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou SOCK \_ RAW). |
| IP \_ RECVTOS | sim | sim | DWORD (booliana) | Indica se a pilha IP deve preencher o buffer de controle com uma mensagem que contém o campo de header IPv4 do Tipo de Serviço (TOS) em um datagrama recebido. Quando esse valor for true, [**a função LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retornará dados de controle opcionais que contêm o valor do campo de título IPv4 do TOS do datagrama recebido.  Essa opção permite que o campo de título IPv4 do TOS do datagrama recebido seja retornado na estrutura [**WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) O tipo de mensagem retornado será IP \_ TOS. Todos os bits DSCP e ECN do campo TOS serão retornados.  Essa opção só é válida em soquetes de datagrama (o tipo de soquete deve ser SOCK \_ DGRAM).  |
| IP \_ RECVTTL | sim | sim | DWORD (booliana) | Indica que as informações de salto (TTL) devem ser retornadas [**na função LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Se *optval* for definido como **1** na chamada para [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), a opção será habilitada. Se definido como **0,** a opção será desabilitada.  Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou SOCK \_ RAW). |
| IP \_ TOS | sim | sim | DWORD (booliana) | Não use. As configurações de Tipo de Serviço (TOS) só devem ser definidas usando a API de Qualidade de Serviço. Consulte [Serviços Diferenciados](/previous-versions/windows/desktop/qos/differentiated-services) na seção Qualidade de Serviço do SDK da Plataforma para obter mais informações. |
| IP \_ TTL | sim | sim | DWORD (booliana) | Altera o valor padrão definido pelo provedor de serviços TCP/IP no campo TTL do header IP em datagramas de saída. O suporte à TTL de IP não é necessário; para verificar se há suporte para \_ o \_ IP TTL, use [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para obter as opções atuais. Se **getsockopt** falhar, não há suporte para tTL de \_ IP. |
| IP \_ UNBLOCK \_ SOURCE | | sim | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Adiciona a origem fornecida como um remetente ao grupo e à interface multicast fornecidos. |
| IP \_ UNICAST \_ IF | sim | sim | DWORD (IF \_ INDEX) | Obtém ou define a interface de saída para enviar o tráfego IPv4. Essa opção não altera a interface padrão para receber o tráfego IPv4. Essa opção é importante para computadores multihomed.  O valor de entrada para definir essa opção é um endereço IPv4 de 4 byte na ordem de byte de rede. Esse parâmetro DWORD deve ser um índice de interface na ordem de byte de rede. Qualquer endereço IP no bloco 0.x.x.x (primeiro octeto de 0), exceto o endereço IPv4 0.0.0.0, é tratado como um índice de interface. Um índice de interface é um número de 24 bits e o bloco de endereço IPv4 0.0.0.0/8 não é usado (esse intervalo é reservado). O índice de interface pode ser usado para especificar a interface padrão para enviar tráfego para IPv4. A [**função GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) pode ser usada para obter as informações de índice da interface. Se *optval* for zero, a interface padrão para enviar tráfego será definida como não especificado.  Ao obter essa opção, o *optval* retorna o índice de interface padrão atual para enviar o tráfego IPv4 na ordem de bytes do host. |
| IP_USER_MTU | sim | sim | DWORD | Obtém ou define um limite superior no MTU da camada de IP (em bytes) para o soquete especificado. Se o valor for maior do que a estimativa do sistema do MTU do caminho (que você pode recuperar em um Soquete conectado consultando a opção de soquete **IP_MTU** ), a opção não terá nenhum efeito. Se o valor for inferior, os pacotes de saída maiores que isso serão fragmentados ou não serão enviados, dependendo do valor de **IP_DONTFRAGMENT**. O valor padrão é **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para a segurança de tipo, você deve usar as funções [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) em vez de usar a opção socket diretamente. |
| \_contexto de \_ redirecionamento WFP de IP \_ | sim | sim | WSACMSGHDR com dados de controle | um tipo de dados auxiliar de soquete de datagrama ( \_ tipo cmsg) para indicar o contexto de redirecionamento para um soquete UDP usado por um modo de usuário Windows serviço de redirecionamento WFP (plataforma de filtragem). |
| \_registros de \_ redirecionamento de WFP de IP \_ | sim | sim | WSACMSGHDR com dados de controle | um tipo de dados auxiliar de soquete de datagrama ( \_ tipo cmsg) para indicar o registro de redirecionamento para um soquete UDP usado por um modo de usuário Windows serviço de redirecionamento WFP (plataforma de filtragem). |

## <a name="windows-support-for-ip_proto-options"></a>suporte Windows para opções de IP \_ PROTO

| Opção | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | a partir do Windows 10, versão 1803 | | | | | |
| \_Adicionar \_ Associação de IP | x | x | x | x | x | x |
| IP \_ Adicionar \_ Associação de origem \_ | x | x | x | x | x | x |
| \_origem do bloco de IP \_ | x | x | x | x | x | x |
| IP_DEL_IFLIST | a partir do Windows 10, versão 1803 | | | | | |
| \_DONTFRAGMENT IP | x | x | x | x | x | x |
| \_Associação IP drop \_ | x | x | x | x | x | x |
| \_Associação de \_ origem IP drop \_ | x | x | x | x | x | x |
| IP_GET_IFLIST | a partir do Windows 10, versão 1803 | | | | | |
| \_HDRINCL IP | x | x | x | x | x | x |
| IP_IFLIST | a partir do Windows 10, versão 1803 | | | | | |
| IP \_ multicast \_ se | x | x | x | x | x | x |
| \_loop multicast de IP \_ | x | x | x | x | x | x |
| \_TTL de multicast IP \_ | x | x | x | x | x | x |
| opções de IP \_ | x | x | x | x | x | x |
| chegada de IP \_ original \_ \_ se | x | x | x | x | | |
| \_PKTINFO IP | x | x | x | x | x | x |
| \_difusão de recebimento de IP \_ | x | x | x | x | x | x |
| \_RECVIF IP | a partir do Windows 10, versão 1703 | x | x | x | x | x |
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

no SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o nível de **\_ IP IPPROTO** é definido no arquivo de cabeçalho *Ws2def. h* , que é incluído automaticamente no arquivo de cabeçalho *Winsock2. h* . Algumas das opções de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Ws2ipdef. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Ws2tcpip. h* . As opções restantes de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Wsipv6ok. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* . Os arquivos de cabeçalho *Ws2def. h*, *Ws2ipdef. h* e *Wsipv6ok. h* nunca devem ser usados diretamente.

no SDK da plataforma lançado para o Windows Server 2003 e Windows XP, o nível de **\_ IP IPPROTO** é definido no arquivo de cabeçalho *Winsock2. h* . Algumas das opções de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Ws2tcpip. h* . As opções restantes de soquete de **\_ IP IPPROTO** são definidas no arquivo de cabeçalho *Wsipv6ok. h* , que é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* . O arquivo de cabeçalho *Wsipv6ok. h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | <dl> <dt>Ws2def. h (incluir Winsock2. h); </dt> <dt>Ws2ipdef. h (incluir Ws2tcpip. h); </dt> <dt>Wsipv6ok. h (incluir Winsock2. h)</dt> </dl> |
