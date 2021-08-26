---
title: Descobrir dispositivos e serviços Bluetooth
description: Para facilitar a descoberta de Bluetooth e serviços, o Bluetooth Windows mapeia o protocolo SDP para as interfaces de namespace Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, tarefas, descobrir dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae18f8f7ff8e7c2fcf2623ef9554bc77ec84d4b1d4ea56eced289cc86c12f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004036"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Descobrir dispositivos e serviços Bluetooth

Para facilitar a descoberta de Bluetooth e serviços, o Bluetooth Windows mapeia o protocolo SDP para as interfaces de namespace Windows Sockets. As funções primárias usadas para esse mapeamento são as funções [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e [**WSALookupServiceEnd.**](bluetooth-and-wsalookupserviceend.md) A [**estrutura WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) também é usada em conjunto com essas funções.

Como determinados conceitos e parâmetros do SDP do Bluetooth não são necessariamente mapeados diretamente para a estrutura [**WSAQUERYSET,**](bluetooth-and-wsaqueryset-for-set-service.md) é necessário prestar atenção em como seus membros são criados e usados. Para muitas operações Bluetooth complexas, como a criação de registros SDP, o membro **lpBlob** do **WSAQUERYSET** é usado. Quando essa consideração especial é necessária, ela é descrita especificamente, como em páginas de referência como Bluetooth e [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)e outros.

É importante entender que o registro SDP é separado do controle de soquete. Quando um aplicativo de servidor está preparado para aceitar a conexão do cliente, ele deve chamar a [**função WSASetService**](bluetooth-and-wsasetservice.md) para registrar um registro SDP Bluetooth que corresponde a esse serviço. Esse Bluetooth aplicativo deve chamar a **função WSASetService** novamente antes de fechar, para desregulamentar o registro Bluetooth registro SDP.

Ao usar as funções de mapeamento descritas nesta página, o \_ namespace NS BTH é atribuído.

Para obter mais informações sobre como descobrir dispositivos e serviços, consulte as seguintes páginas de referência:

-   [**Bluetooth e WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth e WSALookupServiceBegin para consulta de dispositivo**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth e WSALookupServiceBegin para Descoberta de Serviço**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth e WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth e WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth e BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth e WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

Você também pode baixar o [exemplo Bluetooth de conexão para](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) um exemplo completo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Bluetooth Programação com Windows soquetes](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Bluetooth de conexão](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




