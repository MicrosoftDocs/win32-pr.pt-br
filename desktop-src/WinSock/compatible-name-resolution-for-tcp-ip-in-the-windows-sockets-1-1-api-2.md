---
description: observe que todas as funções do Windows sockets 1,1 para resolução de nomes são específicas para redes TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: resolução de nome compatível para TCP/IP na API do Windows sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13dfb1a403f782d0349e20729117fe1f4aed01479b01a6c2b5968f1d9bf15f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322296"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>resolução de nome compatível para TCP/IP na API do Windows sockets 1,1

> [!Note]  
> todas as funções do Windows sockets 1,1 para resolução de nomes são específicas para redes TCP/IP IPv4. Os desenvolvedores de aplicativos são altamente desencorajados de continuar a utilizar essas funções específicas de transporte que dão suporte apenas ao IPv4.

 

Os desenvolvedores de aplicativos devem usar as seguintes funções que são independentes de protocolo e dão suporte à resolução de nomes IPv6 e IPv4.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Soquetes 1,1 definidos um número de rotinas usadas para resolução de nomes com redes TCP/IP (IP versão 4). Às vezes, elas são chamadas de funções **getXbyY** e incluem o seguinte:

<dl>

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

As versões assíncronas dessas funções também foram definidas.

<dl>

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

Há também duas funções, agora implementadas no Winsock2.dll, usadas para converter a notação de endereço IPv4 pontilhada de uma cadeia de caracteres e representações binárias, respectivamente.

<dl>

[**\_endereço inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**\_NTOA inet**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

para manter a compatibilidade com versões anteriores estritas com o Windows sockets 1,1, todas as funções somente IPv4 mais antigas continuam a ter suporte desde que pelo menos um provedor de namespace esteja presente e ofereça suporte à \_ família de endereços INET da série af (essas funções não são relevantes para a versão 6 do IP, denotada por AF \_ INET6).

O \_32.dll Ws2 implementa essas funções de compatibilidade em termos dos novos recursos de resolução de nome independentes de protocolo usando uma sequência apropriada [](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)de / chamadas de função **Next** / **end** de WSALookupServiceBegin. Os detalhes de como as funções **getXbyY** são mapeadas para as funções de resolução de nomes são fornecidos abaixo. O WSs2 \_32.dll lida com as diferenças entre as versões assíncronas e síncronas das funções **getXbyY** , de modo que apenas a implementação das funções **getXbyY** síncronas é discutida.

esta seção descreve a resolução de nome compatível para TCP/IP na API do Windows sockets 1,1. A lista a seguir descreve os tópicos nesta seção:

-   [Abordagem básica para GetXbyY na API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Funções getprotobyname e getprotobynumber na API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Funções getservbyname e getservbyport na API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Função gethostbyname na API](gethostbyname-function-in-the-api-2.md)
-   [Função GetHostbyaddr na API](gethostbyaddr-function-in-the-api-2.md)
-   [Função GetHostName na API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
