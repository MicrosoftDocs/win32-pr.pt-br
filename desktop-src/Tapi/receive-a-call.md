---
description: O exemplo de código a seguir demonstra o tratamento de novas notificações de chamada, como localizar ou criar terminais apropriados para renderizar a mídia.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Receber uma chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a78ebf5b77569f8468a8b2c0a30217f4f7430e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757954"
---
# <a name="receive-a-call"></a><span data-ttu-id="dbb1d-103">Receber uma chamada</span><span class="sxs-lookup"><span data-stu-id="dbb1d-103">Receive a Call</span></span>

<span data-ttu-id="dbb1d-104">O exemplo de código a seguir demonstra o tratamento de novas notificações de chamada, como localizar ou criar terminais apropriados para renderizar a mídia.</span><span class="sxs-lookup"><span data-stu-id="dbb1d-104">The following code example demonstrates handling of new call notifications, such as finding or creating appropriate terminals to render the media.</span></span> <span data-ttu-id="dbb1d-105">Este exemplo é uma parte da instrução switch que um aplicativo deve implementar para manipulação de eventos.</span><span class="sxs-lookup"><span data-stu-id="dbb1d-105">This example is a portion of the switch statement an application must implement for event handling.</span></span> <span data-ttu-id="dbb1d-106">O próprio código pode estar contido na implementação de [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)ou o método de **evento** pode postar uma mensagem em um thread de trabalho que contém a opção.</span><span class="sxs-lookup"><span data-stu-id="dbb1d-106">The code itself may be contained in the implementation of [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), or the **Event** method may post a message to a worker thread that contains the switch.</span></span>

<span data-ttu-id="dbb1d-107">Antes de usar este exemplo de código, você deve executar as operações em [inicializar TAPI](initialize-tapi.md), [selecionar um endereço](select-an-address.md)e [registrar eventos](register-events.md).</span><span class="sxs-lookup"><span data-stu-id="dbb1d-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md), [Select an Address](select-an-address.md), and [Register Events](register-events.md).</span></span>

<span data-ttu-id="dbb1d-108">Além disso, você deve executar as operações ilustradas em [selecionar um terminal](select-a-terminal.md) seguindo a recuperação dos ponteiros de interface [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) .</span><span class="sxs-lookup"><span data-stu-id="dbb1d-108">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the retrieval of the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) interface pointers.</span></span>

> [!Note]  
> <span data-ttu-id="dbb1d-109">Este exemplo não tem a verificação de erros e as versões apropriadas para o código de produção.</span><span class="sxs-lookup"><span data-stu-id="dbb1d-109">This example does not have the error checking and releases appropriate for production code.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="dbb1d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbb1d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbb1d-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="dbb1d-111">Events</span></span>](events.md)
</dt> <dt>

[<span data-ttu-id="dbb1d-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="dbb1d-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[<span data-ttu-id="dbb1d-113">**ITTAPI::RegisterCallNotifications**</span><span class="sxs-lookup"><span data-stu-id="dbb1d-113">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[<span data-ttu-id="dbb1d-114">**ITCallNotificationEvent**</span><span class="sxs-lookup"><span data-stu-id="dbb1d-114">**ITCallNotificationEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[<span data-ttu-id="dbb1d-115">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="dbb1d-115">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="dbb1d-116">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="dbb1d-116">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="dbb1d-117">**ITTerminalSupport**</span><span class="sxs-lookup"><span data-stu-id="dbb1d-117">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
