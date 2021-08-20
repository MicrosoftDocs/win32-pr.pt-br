---
title: Bluetooth e BLOB
description: Bluetooth usa a estrutura BLOB para passar ou receber dados específicos de transporte para a estrutura WSAQUERYSET durante chamadas para as funções WSASetService ou WSALookupService\.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth e BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960362e7f6bc6388d3b93bd6e0329e405bdb33ed6e796a5ec5793d402ba0557c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081130"
---
# <a name="bluetooth-and-blob"></a>Bluetooth e BLOB

Bluetooth usa a estrutura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) para passar ou receber dados específicos de transporte para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante chamadas para as funções [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService.** \*

Para uso com Bluetooth e a [**função WSASetService,**](bluetooth-and-wsasetservice.md) os membros da estrutura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) devem ter as seguintes configurações:

-   O **membro cbsize** deve ser definido como o tamanho da estrutura [**BTH SET \_ \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) usada no membro **pBlobData,** em bytes.
-   O **membro pBlobData** deve ser um ponteiro para uma estrutura [**BTH SET \_ \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

Para uso com Bluetooth [e WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)Consulta de Dispositivo , use as seguintes configurações:

-   O **membro cbsize** deve ser definido como o tamanho da estrutura [**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) usada no membro **pBlobData,** em bytes.
-   O **membro pBlobData** deve ser um ponteiro para uma estrutura DE DISPOSITIVO [**DE \_ CONSULTA \_ BTH.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)

Para uso com Bluetooth e [WSALookupServiceBegin para Descoberta](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)de Serviço , use as seguintes configurações:

-   O **membro cbsize** deve ser definido como o tamanho da estrutura [**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) usada no membro **pBlobData,** em bytes.
-   O **membro pBlobData** deve ser um ponteiro para uma estrutura [**BTH \_ QUERY \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)

Para obter mais informações, consulte a seção Comentários na página de referência da estrutura [**BTH \_ SET \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para Descoberta de Serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**DISPOSITIVO DE \_ CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SERVIÇO \_ DE CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**Wsasetservice**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 