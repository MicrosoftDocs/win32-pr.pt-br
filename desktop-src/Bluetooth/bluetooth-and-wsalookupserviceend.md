---
title: Bluetooth e WSALookupServiceEnd
description: Bluetooth usa a função WSALookupServiceEnd para encerrar uma consulta iniciada em uma chamada anterior para WSALookupServiceBegin e, talvez, estendida em chamadas subsequentes para WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd6c893a06fbf586d07e3a2581d1d25626e161508e505dc089d7660267bae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081090"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth e WSALookupServiceEnd

Bluetooth usa a função [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para encerrar uma consulta iniciada em uma chamada anterior para [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)e, talvez, estendida em chamadas subsequentes para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta). A chamada para **WSALookupServiceEnd** encerra a consulta e limpa o contexto.

as etapas para consulta de dispositivo e descoberta de serviço no Bluetooth são suficientemente diferentes para mérito um tratamento separado. para obter mais informações sobre Bluetooth e a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultas de dispositivo, consulte [Bluetooth e WSALookupServiceBegin para consulta de dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). para obter mais informações sobre Bluetooth e a função **WSALookupServiceBegin** para descoberta de serviço, consulte [Bluetooth e WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Descobrir dispositivos e serviços Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para a consulta do dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin para descoberta de serviço](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**\_serviço de consulta do BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 