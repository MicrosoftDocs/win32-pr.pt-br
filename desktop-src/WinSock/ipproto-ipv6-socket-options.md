---
description: As tabelas a seguir descrevem \_ as opções de soquete do IPPROTO IPv6 que se aplicam aos soquetes criados para a família de endereços IPv6 (AF \_ INET6). Consulte as páginas de referência de função getsockopt e setsockopt para obter mais informações sobre como obter e definir opções de soquete.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: Opções de soquete IPPROTO_IPV6
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 86f8156f91e5f7e185319224e06d7bf54e87c6da
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444247"
---
# <a name="ipproto_ipv6-socket-options"></a>Opções de soquete do IPPROTO \_ IPv6

As tabelas a seguir descrevem as opções de soquete do **IPPROTO \_ IPv6** que se aplicam aos soquetes criados para a família de endereços IPv6 (AF \_ INET6). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Algumas opções de soquete exigem mais explicações do que essas tabelas podem ser transmitidas; essas opções contêm links para informações adicionais.

## <a name="options"></a>Opções

| Opção | get | set | Tipo de optval | Descrição |
|-|-|-|-|-|
| chegada de IP \_ original \_ \_ se | sim | sim | DWORD (booliano) | Indica se a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve retornar dados de controle opcionais contendo a interface de chegada original em que o pacote foi recebido para soquetes de datagrama. Essa opção é usada com tecnologias de transição IPv6 (túneis 6to4, ISATAP e Teredo, por exemplo) que fornecem atribuição de endereço e túnel automático de host para host para tráfego IPv6 unicast quando hosts IPv6 devem atravessar redes IP4 para alcançar outras redes IPv6. Os pacotes IPv6 são enviados em túnel como pacotes IPv4. Essa opção permite que a interface IPv4 original em que o pacote foi recebido seja retornada na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  |
| IPV6_ADD_IFLIST | | sim | DWORD (IF_INDEX) | Adiciona um índice de interface ao IFLIST associado à opção **IP_IFLIST** . |
| \_Adicionar \_ Associação de IPv6 | | sim | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Junte o soquete ao grupo de multicast fornecido na interface especificada.  Essa opção só é válida em soquetes de datagrama e brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| IPV6_DEL_IFLIST | | sim | DWORD (IF_INDEX) | Remove um índice de interface do IFLIST associado à opção **IP_IFLIST** . As entradas podem ser removidas somente pelo aplicativo, portanto, lembre-se de que as entradas podem ficar obsoletas depois que uma interface é removida. |
| \_Associação de remoção de IPv6 \_ | | sim | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Deixe o grupo de multicast fornecido da interface fornecida.  Essa opção só é válida em soquetes de datagrama e brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| IPV6_GET_IFLIST | sim | | DWORD [] (IF_INDEX []) | Obtém o IFLIST atual associado à opção **IP_IFLIST** . Retornará um erro se **IP_IFLIST** não estiver habilitado. |
| \_HDRINCL IPv6 | sim | sim | DWORD (booliano) | Indica que o aplicativo fornece o cabeçalho IPv6 em todos os dados de saída. Se o parâmetro *optval* for definido como **1** na chamada para [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), a opção será habilitada. Se *optval* for definido como **0**, a opção será desabilitada. O valor padrão é desabilitada. Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). Um provedor de serviços TCP/IP que dá suporte ao \_ RAW Sock também deve dar suporte a \_ HDRINCL IPv6. |
| \_HOPLIMIT IPv6 | sim | sim | DWORD (booliano) | Indica que as informações de salto (TTL) devem ser retornadas na função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Se *optval* for definido como **1** na chamada para [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), a opção será habilitada. Se definido como **0**, a opção será desabilitada.  Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| IPV6_IFLIST | sim | sim | DWORD (booliano) | Obtém ou define o estado de **IP_IFLIST** do soquete. Quando essa opção é definida como true, a recepção de datagrama é restrita a interfaces que estão no IFLIST. Os datagramas recebidos em outras interfaces são ignorados. IFLIST começa vazio. Use **IP_ADD_IFLIST** e **IP_DEL_IFLIST** para editar o IFLIST. |
| \_Grupo de junção IPv6 \_ | | sim | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Igual ao IPV6 \_ Adicionar \_ Associação |
| \_Grupo de saída IPv6 \_ | | sim | [**\_mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Mesmo que a \_ Associação IPv6 drop \_ |
| \_MTU IPv6 | sim | | DWORD | Obtém a estimativa do sistema da MTU do caminho. O soquete deve estar conectado. |
| \_Descoberta de MTU IPv6 \_ | sim | sim | DWORD (**\_ estado do PMTUD**) | Obtém ou define o estado de descoberta de MTU do caminho para o soquete. O valor padrão é **IP \_ PMTUDISC \_ não \_ definido**. Para soquetes de fluxo, **\_ PMTUDISC IP \_ não \_ definido** e o **IP \_ PMTUDISC \_** executará a descoberta de MTU de caminho. **IP \_ PMTUDISC \_** não e **a \_ \_ investigação de PMTUDISC de IP** DESligará a descoberta de MTU de caminho. Para soquetes de datagramas, se definido como **\_ PMTUDISC \_ IP** , as tentativas de enviar pacotes maiores que a MTU de caminho resultarão em um erro. Se definido como **IP \_ PMTUDISC \_**, os pacotes serão fragmentados de acordo com a interface MTU. Se definido como **\_ \_ investigação de PMTUDISC IP**, as tentativas de enviar pacotes maiores do que a MTU da interface resultarão em um erro.  |
| \_Saltos de multicast IPv6 \_ | sim | sim | DWORD | Obtém ou define o valor de TTL associado ao tráfego de multicast IPv6 no soquete. É ilegal definir o TTL como um valor maior que 255.  Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| \_Multicast IPv6 \_ se | sim | sim | DWORD | Obtém ou define a interface de saída para enviar tráfego de multicast IPv6. Essa opção não altera a interface padrão para receber o tráfego multicast IPv6. Essa opção é importante para computadores de hospedagem múltipla.  O valor de entrada para definir essa opção é um índice de interface de 4 bytes da interface de saída desejada na ordem de bytes do host. A função [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) pode ser usada para obter as informações de índice da interface. Se *optval* for definido como **NULL** na chamada para [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), a interface IPv6 padrão será usada. Se *optval* for zero, a interface padrão para receber multicast será especificada para o envio de tráfego multicast.  Ao obter essa opção, o *optval* retorna o índice de interface padrão atual para enviar tráfego IPv6 Multicast na ordem de bytes do host. |
| \_Loop de multicast IPv6 \_ | sim | sim | DWORD (booliano) | Indica que os dados multicast enviados no soquete serão ecoados para o buffer de recebimento de soquetes se ele também estiver Unido no grupo de multicast de destino. Se *optval* for definido como **1** na chamada para [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), a opção será habilitada. Se definido como **0**, a opção será desabilitada.  Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| [\_PKTINFO IPv6](ipv6-pktinfo.md) | sim | sim | DWORD (booliano) | Indica que as informações de pacote devem ser retornadas pela função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . |
| [\_Nível de proteção IPv6 \_](ipv6-protection-level.md) | sim | sim | INT | Habilita a restrição de um soquete para um escopo especificado, como endereços com o mesmo link local ou o prefixo local do site. Fornece vários níveis de restrição e configurações padrão. Consulte [ \_ \_ nível de proteção IPv6](ipv6-protection-level.md) para obter mais informações. |
| \_RECVIF IPv6 | sim | sim | DWORD (booliano) | Indica se a pilha de IP deve preencher o buffer de controle com detalhes sobre qual interface recebeu um pacote com um soquete de datagrama. Quando esse valor for true, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retornará dados de controle opcionais contendo a interface em que o pacote foi recebido para soquetes de datagrama. Essa opção permite que a interface IPv6 em que o pacote foi recebido seja retornada na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Essa opção só é válida para datagrama e soquetes brutos (o tipo de soquete deve ser SOCK \_ DGRAM ou Sock \_ RAW). |
| \_RECVTCLASS IPv6 | sim | sim | DWORD (booliano) | Indica se a pilha de IP deve preencher o buffer de controle com uma mensagem que contém o campo de cabeçalho IPv6 de classe de tráfego em um datagrama recebido. Quando esse valor for true, a função [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retornará dados de controle opcionais contendo o valor do campo de cabeçalho IPv6 da classe de tráfego do datagrama recebido.  Essa opção permite que o campo de cabeçalho IPv6 da classe de tráfego do datagrama recebido seja retornado na estrutura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . O tipo de mensagem retornado será \_ TCLASS IPv6. Todos os bits DSCP e ECN do campo classe de tráfego serão retornados.  Essa opção só é válida em soquetes de datagrama (o tipo de soquete deve ser SOCK \_ DGRAM).  |
| \_Saltos de unicast IPv6 \_ | sim | sim | DWORD | Obtém ou define o valor do TTL atual associado ao soquete IPv6 para tráfego unicast. É ilegal definir o TTL como um valor maior que 255. |
| Unicast IPV6 \_ \_ se | sim | sim | DWORD (se \_ índice) | Obtém ou define a interface de saída para enviar tráfego IPv6. Essa opção não altera a interface padrão para receber tráfego IPv6. Essa opção é importante para computadores de hospedagem múltipla.  O valor de entrada para definir essa opção é um índice de interface de 4 bytes da interface de saída desejada na ordem de bytes do host. A função [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) pode ser usada para obter as informações de índice da interface. Se *optval* for zero, a interface padrão para enviar tráfego IPv6 será definida como não especificado.  Ao obter essa opção, o *optval* retorna o índice de interface padrão atual para enviar tráfego IPv6 na ordem de bytes do host. |
| IPV6_USER_MTU | sim | sim | DWORD | Obtém ou define um limite superior no MTU da camada de IP (em bytes) para o soquete especificado. Se o valor for maior do que a estimativa do sistema do MTU do caminho (que você pode recuperar em um Soquete conectado consultando a opção de soquete **IPV6_MTU** ), a opção não terá nenhum efeito. Se o valor for inferior, os pacotes de saída maiores que isso serão fragmentados ou não serão enviados, dependendo do valor de **IPV6_DONTFRAG**. O valor padrão é **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Para a segurança de tipo, você deve usar as funções [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) em vez de usar a opção socket diretamente. |
| \_V6ONLY IPv6 | sim | sim | DWORD (booliano) | Indica se um soquete criado para a \_ família de endereços INET6 de AF é restrito apenas a comunicações IPv6. Os soquetes criados para a \_ família de endereços INET6 de AF podem ser usados para comunicações IPv6 e IPv4. Alguns aplicativos podem querer restringir o uso de um soquete criado para a família de \_ endereços de AF INET6 apenas para comunicações IPv6. Quando esse valor é diferente de zero (o padrão no Windows), um soquete criado para a \_ família de endereços INET6 de AF pode ser usado para enviar e receber somente pacotes IPv6. Quando esse valor for zero, um soquete criado para a \_ família de endereços INET6 de AF poderá ser usado para enviar e receber pacotes de e para um endereço IPv6 ou um endereço IPv4. Observe que a capacidade de interagir com endereços IPv4 requer o uso dos endereços IPv4 mapeados. Essa opção de soquete tem suporte no Windows Vista ou posterior. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Suporte do Windows para \_ Opções de soquete IPv6 IPPROTO

| Opção | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| chegada de IP \_ original \_ \_ se | x | x | x | | |
| IPV6_ADD_IFLIST | Começando com Windows 10, versão 1803 | | | | |
| IPV6 \_ ADD \_ MEMBERSHIP | x | x | x | x | x |
| IPV6_DEL_IFLIST | Começando com Windows 10, versão 1803 | | | | |
| IPV6 \_ DROP \_ MEMBERSHIP | x | x | x | x | x |
| IPV6_GET_IFLIST | Começando com Windows 10, versão 1803 | | | | |
| IPV6 \_ HDRINCL | x | x | x | x | x |
| IPV6 \_ HOPLIMIT | x | x | x | x | x |
| IPV6_IFLIST | Começando com Windows 10, versão 1803 | | | | |
| GRUPO DE JUNÇÃO IPV6 \_ \_ | x | x | x | x | x |
| IPV6 \_ LEAVE \_ GROUP | x | x | x | x | x |
| SALTOS MULTICAST IPV6 \_ \_ | x | x | x | x | x |
| IPV6 \_ MULTICAST \_ IF | x | x | x | x | x |
| IPV6 \_ MULTICAST \_ LOOP | x | x | x | x | x |
| IPV6 \_ PKTINFO | x | x | x | x | x |
| [NÍVEL DE PROTEÇÃO \_ IPV6 \_](ipv6-protection-level.md) | x | x | x | x | x |
| IPV6 \_ RECVIF | x | x | x | x | x |
| SALTOS UNICAST IPV6 \_ \_ | x | x | x | x | x |
| IPV6 \_ UNICAST \_ IF | x | x | x | x | x |
| IPV6 \_ V6ONLY | x | x | x | x | x |

<br/>

| Opção | Windows Server 2003 | Windows XP |
|-|-|-|
| chegada de IP \_ original \_ \_ se | | |
| IPV6_ADD_IFLIST | | |
| \_Adicionar \_ Associação de IPv6 | x | x |
| IPV6_DEL_IFLIST | | |
| \_Associação de remoção de IPv6 \_ | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| IPV6 \_ HOPLIMIT x | x |
| IPV6_IFLIST | | |
| \_Grupo de junção IPv6 \_ | x | x |
| \_Grupo de saída IPv6 \_ | x | x |
| \_Saltos de multicast IPv6 \_ | x | x |
| \_Multicast IPv6 \_ se | x | x |
| \_Loop de multicast IPv6 \_ | x | x |
| \_PKTINFO IPv6 | x | x |
| [\_Nível de proteção IPv6 \_](ipv6-protection-level.md) | x | x |
| \_RECVIF IPv6 | | |
| \_Saltos de unicast IPv6 \_ | x | x |
| Unicast IPV6 \_ \_ se | | |
| \_V6ONLY IPv6 | | |

## <a name="remarks"></a>Comentários

No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o nível de **IPPROTO \_ IPv6** é definido no arquivo de cabeçalho *Ws2def. h* , que é incluído automaticamente no arquivo de cabeçalho *Winsock2. h* . As opções de soquete **\_ IPv6 IPPROTO** são definidas no arquivo de cabeçalho *Ws2ipdef. h* , que é incluído automaticamente no arquivo de cabeçalho *Ws2tcpip. h* . Os arquivos de cabeçalho *Ws2def. h* e *Ws2ipdef. h* nunca devem ser usados diretamente.

A chegada de IP \_ original \_ se a \_ opção de soquete tiver suporte no Windows Server 2008 R2, bem como no Windows 7.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | <dl> <dt>Ws2def. h (incluir Winsock2. h); </dt> <dt>Winsock2. h no Windows Server 2003 e no Windows XP</dt> </dl> |
