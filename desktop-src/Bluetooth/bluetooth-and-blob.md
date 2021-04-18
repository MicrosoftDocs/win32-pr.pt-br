---
title: Bluetooth e BLOB
description: O Bluetooth usa a estrutura de BLOB para passar ou receber dados específicos de transporte para a estrutura WSAQUERYSET durante chamadas para as funções WSASetService ou WSALookupService.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth e BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753000"
---
# <a name="bluetooth-and-blob"></a>Bluetooth e BLOB

O Bluetooth usa a estrutura de [**blob**](/windows/desktop/api/nspapi/ns-nspapi-blob) para passar ou receber dados específicos de transporte para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante chamadas para as funções [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService** \* .

Para uso com o Bluetooth e a função [**WSASetService**](bluetooth-and-wsasetservice.md) , os membros da estrutura de [**BLOBs**](/windows/desktop/api/nspapi/ns-nspapi-blob) devem ter as seguintes configurações:

-   O membro **cbSize** deve ser definido como o tamanho da estrutura [**de \_ \_ serviço do conjunto de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) usado no membro **pBlobData** , em bytes.
-   O membro **pBlobData** deve ser um ponteiro para uma estrutura de [**\_ \_ serviço de conjunto de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

Para usar com Bluetooth e [WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use as seguintes configurações:

-   O membro **cbSize** deve ser definido como o tamanho da estrutura [**de \_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) usada no membro **pBlobData** , em bytes.
-   O membro **pBlobData** deve ser um ponteiro para uma estrutura de [**\_ \_ dispositivo de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .

Para usar com o Bluetooth e o [WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use as seguintes configurações:

-   O membro **cbSize** deve ser definido como o tamanho da estrutura [**do \_ \_ serviço de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) usada no membro **pBlobData** , em bytes.
-   O membro **pBlobData** deve ser um ponteiro para uma estrutura de [**\_ \_ serviço de consulta BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .

Para obter mais informações, consulte a seção comentários na página de referência da estrutura de [**\_ \_ serviço do BTH Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_dispositivo de consulta BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_serviço de consulta do BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ definir \_ serviço**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 