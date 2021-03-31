---
title: Bluetooth e getaddrinfo
description: A função getaddrinfo fornece a tradução do nome do host para tratar de transportes baseados em IP. Como a função getaddrinfo é específica para transportes baseados em IP, ela falha em soquetes Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth e Bluetooth getaddrinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641737"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth e getaddrinfo

A função [**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornece a tradução do nome do host para tratar de transportes baseados em IP. Como a função **Getaddrinfo** é específica para transportes baseados em IP, ela falha em soquetes Bluetooth.

Para executar a conversão do nome do host para tratar de soquetes Bluetooth, use a função [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) com **\_ contêineres Lup** para consultar dispositivos remotos e, em seguida, procure um nome remoto correspondente e um endereço correspondente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 