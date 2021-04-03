---
title: Provedores de dispositivo
description: Os provedores de dispositivo são objetos registrados que o computador inicia em todas as inicializações do sistema.
ms.assetid: 80c08993-0a8b-4ee9-93cd-bcc3c00e843b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fac270342830045fc3bac9f0573f283d87dc6a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084599"
---
# <a name="device-providers"></a>Provedores de dispositivo

Os provedores de dispositivo são objetos registrados que o computador inicia em todas as inicializações do sistema. Os provedores de dispositivo registram e cancelam o registro de dispositivos em execução com o host do dispositivo em resposta a algum evento. Esses dispositivos são dispositivos que foram iniciados automaticamente no momento da inicialização do sistema. Por motivos de segurança, um provedor de dispositivo deve geralmente ser executado como [LocalService](/windows/desktop/Services/localservice-account), em vez de [LocalSystem](/windows/desktop/Services/localsystem-account).

Os provedores de dispositivo podem ser usados para dispositivos transitórios. Os provedores de dispositivos também podem ser usados para ligar dispositivos à mídia sondada. Por exemplo, um dispositivo periférico, como um player digital de música, é conectado a um computador por meio de uma porta serial. Para expor o player de música como um dispositivo baseado em UPnP, é necessário um objeto de controle de dispositivo e um conjunto de objetos de serviço. Esses objetos implementam as ações do player de música baseado em UPnP como comandos seriais. No entanto, o player de música deve estar conectado à porta serial e disponível para controle antes que esses objetos sejam registrados.

Como a porta serial não oferece um mecanismo de notificação explícito quando os dispositivos estão conectados, o código de sondagem é necessário. Esse código pode ser implementado em um objeto de provedor de dispositivo, em um serviço ou em um aplicativo autônomo. Quando o computador é iniciado, o host do dispositivo instancia o objeto do provedor do dispositivo e, em seguida, invoca o método [**inicial**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) . Quando o provedor de dispositivo detecta a presença de um dispositivo player de música, ele instancia o objeto de controle de dispositivo apropriado e o registra chamando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice). Esse método publica o dispositivo e o anuncia para a rede baseada em UPnP.

A mesma funcionalidade também pode ser obtida com a implementação de um serviço que sonda a porta serial. No entanto, os provedores de dispositivos simplificam as coisas exigindo apenas a funcionalidade básica — a sondagem — a ser implementada, pois os provedores de dispositivos dependem do host do dispositivo para iniciá-los e pará-los. O uso de provedores de dispositivos é mais simples do que a implementação de um serviço.

No momento do registro, e em cada inicialização subsequente do sistema, o computador instancia o objeto de provedor do dispositivo e, em seguida, invoca o método [**IUPnPDeviceProvider:: Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) , passando-o para a cadeia de inicialização especificada durante o registro.

Depois que o método [**Start**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-start) é chamado, o provedor do dispositivo executa qualquer processamento necessário e, quando necessário, o provedor do dispositivo registra os dispositivos chamando [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), conforme descrito na seção [registrando um dispositivo hospedado com o host do dispositivo](registering-a-hosted-device-with-the-device-host.md).

Quando o computador é desligado, o host do dispositivo invoca o método [**IUPnPDeviceProvider:: Stop**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdeviceprovider-stop) para indicar que o provedor do dispositivo encerra suas operações.

 

 