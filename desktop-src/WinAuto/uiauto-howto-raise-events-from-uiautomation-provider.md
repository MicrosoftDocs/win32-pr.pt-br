---
title: Como auar eventos de um provedor Automação da Interface do Usuário dados
description: Este tópico contém um código de exemplo que mostra como um provedor Automação da Interface do Usuário Microsoft gera um evento.
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75717dfcccaca5f62ac3431f9b3decb01842ce9bc696d07bfff54f35ffc13640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133289"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>Como auar eventos de um provedor Automação da Interface do Usuário dados

Este tópico contém um código de exemplo que mostra como um provedor Automação da Interface do Usuário Microsoft gera um evento.

O código de exemplo a seguir mostra um método de um aplicativo que implementa um botão personalizado. O aplicativo chama o método sempre que o botão personalizado é invocado. O método verifica se algum cliente está escutando eventos e, nesse caso, gera o evento [**\_ UIA Invoke \_ InvokedEventId**](uiauto-event-ids.md) para notificar os clientes de que o botão foi invocado.


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

**Conceitual**
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Tópicos de ida e Automação da Interface do Usuário provedores](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




