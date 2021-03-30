---
description: O provedor WDM (Windows Driver Model) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Provedor WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d96ce356214f2788d3608b2ba85943e607394cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647702"
---
# <a name="wdm-provider"></a>Provedor WDM

O provedor WDM (Windows Driver Model) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo WDM. As classes para drivers de hardware residem no "root \\ WMI namespace".

As classes WDM são definidas principalmente no WMI. mof.

O WDM é uma interface de sistema operacional por meio da qual os componentes de hardware fornecem informações e notificação de eventos. O provedor WDM é uma classe, instância, evento e provedor de métodos que permite que os aplicativos de gerenciamento acessem dados e eventos de drivers de dispositivo habilitados para WMI para WDM. As classes criadas pelo provedor WDM para representar os dados de driver de dispositivo residem apenas no namespace "root \\ WMI". Esse namespace já deve existir antes que o provedor WDM processe os drivers WDM instalados.

O provedor WDM registra informações sobre as operações de WDM no arquivo WmiProv. log. Para obter mais informações, consulte [arquivos de log do WMI](/windows/desktop/WmiSdk/wmi-log-files).

Como uma classe, instância, método e provedor de eventos, o provedor WDM implementa a interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) padrão, bem como os seguintes métodos de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) :

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

O provedor WDM dá suporte ao evento [**WmiEvent**](/windows/desktop/WmiCoreProv/wmievent) extrínsecos, que notifica o WMI sobre eventos de drivers baseados em WDM. Você pode registrar seus consumidores de eventos para eventos **WmiEvent** como faria com qualquer outro evento. Para obter mais informações, consulte [recebendo um evento WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event). Nenhum evento de criação de classe é gerado ao iniciar um driver.

O provedor WDM dá suporte à seguinte classe:

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Acessando dados de drivers de dispositivo](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
