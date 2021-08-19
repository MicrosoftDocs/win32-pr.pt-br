---
title: Cancelando o registro de um dispositivo
description: Use o método IUPnPRegistrar UnregisterDevice para cancelar o registro de um dispositivo.
ms.assetid: 4f7624e3-4d60-406d-8521-1dfc9aee4408
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ff8eeb99ec0ba697c301e8cc15100bd06c0323b95f4099329c46729ceba9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999486"
---
# <a name="unregistering-a-device"></a>Cancelando o registro de um dispositivo

Use o método [**IUPnPRegistrar:: UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice) para cancelar o registro de um dispositivo. O registro do dispositivo pode ser cancelado (removido do host do dispositivo) de forma temporária ou permanente, dependendo do valor de *fPermanent*. Os desenvolvedores devem remover os dispositivos temporariamente se os dispositivos forem registrados novamente e os dispositivos devem usar o mesmo UDN. Caso contrário, os dispositivos serão removidos permanentemente.

O GUID usado para cancelar o registro não é o UDN. Você deve usar a ID retornada a você por [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) ou [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

> [!Note]  
> Você pode liberar o objeto [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Somente a ID deve ser armazenada em cache.

 

Se *fPermanent* for **false**, o dispositivo será removido temporariamente. Use a interface [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar) para registrar novamente o dispositivo. Os métodos [**IUPnPReregistrar:: ReregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice) e [**IUPnPReregistrar:: ReregisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice) usam o mesmo UDN ou UDNs, no caso de dispositivos aninhados, gerados anteriormente pelo host do dispositivo para o dispositivo não registrado.

Se *fPermanent* for **true**, o dispositivo será removido permanentemente do host do dispositivo. O registro desse dispositivo novamente no mesmo computador cria um UDN diferente daquele criado anteriormente.

> [!Note]  
> Quando um dispositivo é registrado várias vezes no mesmo computador, o host do dispositivo gera UDNs diferentes para cada instância do dispositivo.

 

 

 




