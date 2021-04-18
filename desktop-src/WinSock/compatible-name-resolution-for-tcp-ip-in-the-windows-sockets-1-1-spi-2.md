---
description: O Windows Sockets 1,1 definiu várias rotinas que foram usadas para a resolução de nomes IPv4 com redes TCP/IP. Essas são normalmente chamadas de funções GetXbyY e incluem o seguinte.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Resolução de nomes compatível com TCP/IP no SPI do Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781147"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>Resolução de nomes compatível com TCP/IP no SPI do Windows Sockets 1,1

O Windows Sockets 1,1 definiu várias rotinas que foram usadas para a resolução de nomes IPv4 com redes TCP/IP. Essas são normalmente chamadas de funções **GetXbyY** e incluem o seguinte.

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

As versões assíncronas dessas funções também foram definidas.

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Essas funções são específicas para redes TCP/IP; os desenvolvedores de aplicativos independentes de protocolo não são incentivados de continuar a utilizar essas funções específicas de transporte. No entanto, para manter a compatibilidade com versões anteriores estritas com o Windows Sockets 1,1, as funções anteriores continuam com suporte desde que pelo menos um provedor de namespace esteja presente e ofereça suporte à \_ família de endereços inet da série AF.

O *Ws2 \_32.dll* implementa essas funções de compatibilidade em termos dos novos recursos de resolução de nome independentes de protocolo usando uma sequência apropriada de chamadas de função [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . Os detalhes de como as funções **GetXbyY** são mapeadas para as funções de resolução de nomes são fornecidos abaixo. O ws2 \_32.dll lida com as diferenças entre as versões assíncronas e síncronas das funções **GetXbyY** , para que apenas a implementação das funções **GetXbyY** síncronas seja discutida.

 

 
