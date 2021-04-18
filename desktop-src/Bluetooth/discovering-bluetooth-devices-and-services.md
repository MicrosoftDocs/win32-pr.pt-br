---
title: Descobrir dispositivos e serviços Bluetooth
description: Para facilitar a descoberta de dispositivos e serviços Bluetooth, o Windows mapeia o protocolo de descoberta de serviço do Bluetooth (SDP) para as interfaces de namespace do Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tarefas, descobrindo dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2020
ms.locfileid: "105756467"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Descobrir dispositivos e serviços Bluetooth

Para facilitar a descoberta de dispositivos e serviços Bluetooth, o Windows mapeia o protocolo de descoberta de serviço do Bluetooth (SDP) para as interfaces de namespace do Windows Sockets. As funções primárias usadas para esse mapeamento são as funções [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) . A estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) também é usada em conjunto com essas funções.

Como determinados conceitos e parâmetros do SDP do Bluetooth não são necessariamente mapeados diretamente para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) , a atenção deve ser paga sobre como seus membros são criados e usados. Para muitas operações de Bluetooth complexas, como a criação de registros SDP, o membro **lpBlob** do **WSAQUERYSET** é usado. Quando essa consideração especial é necessária, ela é descrita especificamente, como em páginas de referência como [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), entre outras.

É importante entender que o registro SDP é separado do controle de soquete. Quando um aplicativo de servidor está preparado para aceitar a conexão do cliente, ele deve chamar a função [**WSASetService**](bluetooth-and-wsasetservice.md) para registrar um registro SDP do Bluetooth que corresponda a esse serviço. Esse aplicativo Bluetooth deve chamar a função **WSASetService** novamente antes de fechar, para cancelar o registro de registros de SDP do Bluetooth.

Ao usar as funções de mapeamento descritas nesta página, o \_ namespace NS BTH é atribuído.

Para obter mais informações sobre como descobrir dispositivos e serviços, consulte as seguintes páginas de referência:

-   [**Bluetooth e WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth e WSALookupServiceBegin para consulta de dispositivo**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth e WSALookupServiceBegin para descoberta de serviço**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth e WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth e BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth e WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

Você também pode baixar o [exemplo de conexão Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) para obter um exemplo completo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programação de Bluetooth com Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Exemplo de conexão Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




