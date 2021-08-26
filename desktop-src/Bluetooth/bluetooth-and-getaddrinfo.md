---
title: Bluetooth e getaddrinfo
description: A função getaddrinfo fornece tradução do nome do host para o endereço para transporte baseado em IP. Como a função getaddrinfo é específica para transporte baseado em IP, ela falha em Bluetooth soquetes.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth e getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9faea4cebf9eee183942da04f39dfae123feea4900483d27ae2d70d8cb5b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004526"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth e getaddrinfo

A [**função getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornece tradução do nome do host para o endereço para transporte baseado em IP. Como a **função getaddrinfo** é específica para transporte baseado em IP, ela falha em Bluetooth soquetes.

Para executar a conversão do nome do host para o endereço de soquetes do Bluetooth, use a função [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) com CONTÊINERES LUP para consultar **\_ dispositivos remotos** e, em seguida, pesquise um Nome Remoto correspondente específico e o endereço correspondente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 