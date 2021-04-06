---
title: Controlando dispositivos
description: Os dispositivos baseados em UPnP são controlados pelos serviços que eles expõem.
ms.assetid: 4edca439-f767-41e6-97bb-ead751930714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a72a4ffdf91bca358124dbb0a0d95ff9a61e30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822884"
---
# <a name="controlling-devices"></a>Controlando dispositivos

Os dispositivos baseados em UPnP são controlados pelos serviços que eles expõem. Um serviço UPnP é a menor entidade controláveis na arquitetura UPnP. Os dispositivos expõem um serviço para cada função primária que eles executam. Dispositivos complexos são normalmente compostos por vários serviços simples e outros dispositivos.

Um serviço consiste em um conjunto de variáveis de estado e um conjunto de ações que um aplicativo pode invocar para operar nessas variáveis de estado. Na API do ponto de controle com tecnologia UPnP, os serviços são representados por objetos de **serviço** que expõem a interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .

Um tipo de serviço define as variáveis de estado e ações com suporte em um serviço específico. Por exemplo, o tipo de serviço para um serviço de relógio define ações **getTime** e **setTime** , juntamente com uma variável de estado de **tempo** .

Uma ID de serviço diferencia vários tipos de serviço comuns em um único dispositivo. Por exemplo, pode haver dois serviços de relógio em um relógio de alarme, um para o relógio regular e o outro para o alarme. Precisa haver uma maneira de diferenciar entre os dois serviços, que têm tipos de serviço idênticos. A ID de serviço fornece uma maneira exclusiva de identificar uma instância de um tipo de serviço. Em seguida, essa ID de serviço é usada para acessar o serviço correto da coleção [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices) , porque o tipo de serviço não é um identificador exclusivo. A interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) também permite que os aplicativos registrem uma função de retorno de chamada com o objeto de serviço. Quando o valor da variável de estado de um serviço é alterado, o objeto de serviço invoca o retorno de chamada registrado para notificar a aplicação da alteração. A estrutura UPnP também invoca esse retorno de chamada para notificar aplicativos quando uma instância de serviço fica indisponível. O serviço pode ficar indisponível por vários motivos, incluindo uma falha de rede transitória.

Para mais informações, consulte os seguintes tópicos:

-   [Obtendo objetos de serviço](obtaining-service-objects.md)
-   [Registrando um retorno de chamada](registering-a-callback.md)
-   [Consultando variáveis de estado](querying-state-variables.md)
-   [Invocando ações](invoking-actions.md)

 

 




