---
description: A tabela a seguir descreve \_ as opções de soquete UDP IPPROTO que se aplicam aos soquetes criados para as famílias de endereços IPv4 e IPv6 (AF \_ inet e AF \_ INET6) com o parâmetro Protocol para a função socket especificada como UDP (IPPROTO \_ UDP).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: Opções de soquete IPPROTO_UDP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 6f1f25ebae34d7db4290ab23bbf799fc0e0b68df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784529"
---
# <a name="ipproto_udp-socket-options"></a>\_Opções de soquete UDP IPPROTO

A tabela a seguir descreve as opções de soquete **\_ UDP IPPROTO** que se aplicam aos soquetes criados para as famílias de endereços IPv4 e IPv6 (AF \_ inet e AF \_ INET6) com o parâmetro *Protocol* para a função [**Socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) especificada como UDP (IPPROTO \_ UDP). Consulte as páginas de referência de função [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Opções

| Opção | Obter | Definir | Tipo de optval | Descrição |
|-|-|-|-|-|
| \_ \_ Cobertura de soma de verificação UDP (Ws2tcpip. h) | sim | sim | DWORD (booliano) | Quando **true**, os datagramas UDP são enviados com uma soma de verificação. |
| UDP \_ NoChecksum (Ws2tcpip. h) | sim | sim | DWORD (booliano) | Quando **true**, os datagramas UDP são enviados com a soma de verificação zero. Necessário para provedores de serviços. Se um provedor de serviços não tiver um mecanismo para desabilitar o cálculo da soma de verificação UDP, ele poderá simplesmente armazenar essa opção sem realizar nenhuma ação. Essa opção não tem suporte para IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef. h; inclui Ws2tcpip. h) | sim | sim | DWORD | Quando definido como um valor diferente de zero, vários datagramas recebidos podem ser agrupados em um único buffer de mensagens antes de serem indicados para seu aplicativo. O valor da opção representa o tamanho máximo da mensagem em bytes para mensagens Unidas que podem ser indicadas para seu aplicativo. Mensagens não Unidas maiores que o valor da opção ainda podem ser indicadas. O valor padrão é 0 (sem União). Os datagramas serão agrupados somente se forem originados do mesmo endereço de origem e porta. Todos os datagrams Unidos serão do mesmo tamanho &mdash; , exceto o último datagrama, que pode ser menor. Se seu aplicativo quiser recuperar os tamanhos de datagramas (exceto o último datagrama, que pode diferir) que foram agrupados, você deverá usar uma API de recebimento que dê suporte a informações de controle (como [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)). O tamanho de todos, exceto a última mensagem, pode ser encontrado na mensagem de controle de **UDP_COALESCED_INFO** , que é do tipo DWORD. Para a segurança de tipo, seu aplicativo deve usar as funções [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) e [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) em vez da opção socket diretamente. |
| UDP_SEND_MSG_SIZE (ws2ipdef. h; inclui Ws2tcpip. h) | sim | sim | DWORD | Quando definido como um valor diferente de zero, os buffers enviados pelo seu aplicativo são divididos em várias mensagens pela pilha de rede. O valor da opção representa o tamanho de cada mensagem desfeita. O valor da opção é representado em bytes. O tamanho do último segmento pode ser menor que o valor da opção. O valor padrão é 0 (sem segmentação). Seu aplicativo deve definir um valor menor do que o MTU do caminho para os destinos a fim de evitar a fragmentação de IP. Para a segurança de tipo, seu aplicativo deve usar as funções [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) e [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) em vez da opção socket diretamente. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Suporte herdado do Windows para \_ Opções de UDP IPPROTO

**UDP \_ A \_ cobertura de soma de verificação** não está disponível no Windows 2000 e no Windows NT4. **UDP \_ A \_ cobertura de soma de verificação** e o UDP NoChecksum não estão disponíveis no Windows 9x/me. **\_** 

## <a name="remarks"></a>Comentários

No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o nível de **\_ UDP IPPROTO** é definido no arquivo de cabeçalho *Ws2def. h* , que é incluído automaticamente no arquivo de cabeçalho *Winsock2. h* . As opções de soquete **\_ UDP IPPROTO** são definidas no arquivo de cabeçalho *Ws2tcpip. h* . O arquivo de cabeçalho *Ws2def. h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro<br/> | <dl> <dt>ws2ipdef. h (incluir Ws2tcpip. h) e Ws2tcpip. h</dt> <dt>Winsock2. h no Windows Server 2003, Windows XP e Windows 2000</dt> </dl> |
