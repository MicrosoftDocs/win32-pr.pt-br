---
description: O exemplo de código a seguir demonstra o tratamento de novas notificações de chamada, como localizar ou criar terminais apropriados para renderizar a mídia.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Receber uma chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e4ce02ec11a1373d16b9b9ebd0fba29313b1d532175894c6fd1b12a38e2bf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060464"
---
# <a name="receive-a-call"></a>Receber uma chamada

O exemplo de código a seguir demonstra o tratamento de novas notificações de chamada, como localizar ou criar terminais apropriados para renderizar a mídia. Este exemplo é uma parte da instrução switch que um aplicativo deve implementar para manipulação de eventos. O próprio código pode estar contido na implementação de [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)ou o método Event pode postar uma mensagem em um thread de trabalho que contém a opção . 

Antes de usar este exemplo de código, você deve executar as operações em [Inicializar TAPI,](initialize-tapi.md)Selecionar um [Endereço](select-an-address.md)e [Registrar Eventos](register-events.md).

Além disso, você deve executar as operações ilustradas em Selecionar um Terminal após [a](select-a-terminal.md) recuperação dos ponteiros de interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITAddress.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)

> [!Note]  
> Este exemplo não tem a verificação de erro e as versões apropriadas para o código de produção.

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Eventos](events.md)
</dt> <dt>

[**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
