---
description: A tabela a seguir descreve as opções de soquete UDP IPPROTO que se aplicam a soquetes criados para as famílias de endereços IPv4 e IPv6 (AF INET e AF INET6) com o parâmetro de protocolo para a função de soquete especificada como \_ \_ \_ UDP \_ (IPPROTO UDP).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: Opções de soquete IPPROTO_UDP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 763e45a78ffd8bfed15d09f4e77bc17be71ccc110499d8937b60b49294f499c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051474"
---
# <a name="ipproto_udp-socket-options"></a>Opções de \_ soquete UDP IPPROTO

A tabela a seguir descreve as opções de soquete **\_ UDP IPPROTO** que se aplicam a soquetes criados para as famílias de endereços IPv4 e IPv6 (AF INET e AF INET6) com o parâmetro de protocolo para a função de soquete especificada como \_ \_ UDP  [](/windows/win32/api/Winsock2/nf-winsock2-socket) \_ (IPPROTO UDP). Consulte as páginas de referência da função [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32.**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

## <a name="options"></a>Opções

| Opção | Obter | Definir | Tipo de aceitação | Descrição |
|-|-|-|-|-|
| UDP \_ CHECKSUM \_ COVERAGE (ws2tcpip.h) | sim | sim | DWORD (booliana) | Quando **TRUE**, os datagramas UDP são enviados com uma verificação. |
| UDP \_ NOCHECKSUM (ws2tcpip.h) | sim | sim | DWORD (booliana) | Quando **TRUE**, os datagramas UDP são enviados com a verificação de zero. Necessário para provedores de serviços. Se um provedor de serviços não tiver um mecanismo para desabilitar o cálculo de verificação UDP, ele poderá simplesmente armazenar essa opção sem tomar nenhuma ação. Não há suporte para essa opção para IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef.h; inclua ws2tcpip.h) | sim | sim | DWORD | Quando definido como um valor não zero, vários datagramas recebidos podem ser unidos em um único buffer de mensagem antes de serem indicados para seu aplicativo. O valor da opção representa o tamanho máximo da mensagem em bytes para mensagens em coalesced que podem ser indicadas para seu aplicativo. Mensagens não coalescadas maiores que o valor da opção ainda podem ser indicadas. O valor padrão é 0 (sem união). Os datagramas só serão coalescados se originados do mesmo endereço de origem e porta. Todos os datagramas coalesced terão o mesmo tamanho, exceto o &mdash; último datagrama, que pode ser menor. Se seu aplicativo quiser recuperar os tamanhos de datagrama (exceto o último datagrama, que pode ser diferente) que foram coalescados, você deverá usar uma API de recebimento que dá suporte a informações de controle [**(como LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) O tamanho de todos, mas a última mensagem pode ser encontrado **na UDP_COALESCED_INFO** de controle, que é do tipo DWORD. Para segurança de tipo, seu aplicativo deve usar as funções [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) e [WSASetUdpRecvMaxCoalescedSize em](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) vez da opção de soquete diretamente. |
| UDP_SEND_MSG_SIZE (ws2ipdef.h; inclua ws2tcpip.h) | sim | sim | DWORD | Quando definido como um valor não zero, os buffers enviados pelo aplicativo são divididos em várias mensagens pela pilha de rede. O valor da opção representa o tamanho de cada mensagem dividida. O valor da opção é representado em bytes. O tamanho do último segmento pode ser menor que o valor da opção. O valor padrão é 0 (sem segmentação). Seu aplicativo deve definir um valor menor que a MTU do caminho para os destinos para evitar a fragmentação de IP. Para segurança de tipo, seu aplicativo deve usar as funções [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) e [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) em vez da opção de soquete diretamente. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Suporte de Windows para opções de UDP IPPROTO \_

**UDP \_ CHECKSUM \_ COVERAGE não** está disponível Windows 2000 e no Windows NT4. **UDP \_ CHECKSUM \_ COVERAGE e** **UDP \_ NOCHECKSUM** não estão disponíveis Windows 9x/Me. 

## <a name="remarks"></a>Comentários

No SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e posterior, a organização dos arquivos de título foi alterada e o nível **\_ de UDP IPPROTO** é definido no arquivo de título *Ws2def.h,* que é incluído automaticamente no arquivo de título *Winsock2.h.* As **opções de soquete \_ UDP IPPROTO** são definidas no arquivo de título *Ws2tcpip.h.* O *arquivo de título Ws2def.h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro<br/> | <dl> <dt>ws2ipdef.h (inclua ws2tcpip.h) e ws2tcpip.h</dt> <dt>Winsock2.h no Windows Server 2003, Windows XP e Windows 2000</dt> </dl> |
