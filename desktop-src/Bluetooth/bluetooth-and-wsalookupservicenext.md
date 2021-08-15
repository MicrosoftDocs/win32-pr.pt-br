---
title: Bluetooth e WSALookupServiceNext
description: Bluetooth usa a função WSALookupServiceNext para corresponder às consultas especificadas em uma chamada anterior para WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- Wsalookupservicenext
- Bluetooth e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010388"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth e WSALookupServiceNext

Bluetooth usa a [**função WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para corresponder às consultas especificadas em uma chamada anterior para [**WSALookupServiceBegin.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) Os resultados da **função WSALookupServiceNext** são determinados pelas configurações definidas na estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passada na chamada de função **WSALookupServiceBegin** inicial.

As etapas para a consulta de dispositivo e a descoberta de serviço Bluetooth são suficientemente diferentes para tratar separadamente. Para obter mais informações sobre Bluetooth e a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultas de dispositivo, consulte [Bluetooth e WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)Consulta de Dispositivo . Para obter mais informações sobre Bluetooth e a função **WSALookupServiceBegin** para descoberta de serviço, consulte [Bluetooth e WSALookupServiceBegin para](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)Descoberta de Serviço .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descobrir dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para Descoberta de Serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[**SERVIÇO \_ DE CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**Wsalookupserviceend**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**Wsalookupservicenext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 