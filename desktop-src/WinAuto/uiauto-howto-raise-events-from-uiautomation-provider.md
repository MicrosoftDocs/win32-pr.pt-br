---
title: Como gerar eventos de um provedor de automação de interface do usuário
description: Este tópico contém um código de exemplo que mostra como um provedor de automação de interface do usuário da Microsoft gera um evento.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791274"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Como gerar eventos de um provedor de automação de interface do usuário

Este tópico contém um código de exemplo que mostra como um provedor de automação de interface do usuário da Microsoft gera um evento.

O código de exemplo a seguir mostra um método de um aplicativo que implementa um botão personalizado. O aplicativo chama o método sempre que o botão personalizado é invocado. O método verifica se algum cliente está ouvindo eventos e, em caso afirmativo, gera o evento [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) para notificar os clientes que o botão foi invocado.


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Tópicos de instruções para provedores de automação de interface do usuário](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




