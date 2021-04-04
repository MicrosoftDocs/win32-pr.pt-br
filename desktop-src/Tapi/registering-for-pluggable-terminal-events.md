---
description: O processo de registro de eventos ocorre quando o terminal é selecionado por um fluxo.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Registrando para eventos de terminal conectável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837478"
---
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="c1315-103">Registrando para eventos de terminal conectável</span><span class="sxs-lookup"><span data-stu-id="c1315-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="c1315-104">O processo de registro de eventos ocorre quando o terminal é selecionado por um fluxo.</span><span class="sxs-lookup"><span data-stu-id="c1315-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="c1315-105">Na implementação do aplicativo de terminal do método [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) , podemos usar a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) do terminal que foi anexado ao fluxo e chamar **QueryInterface** para localizar [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span><span class="sxs-lookup"><span data-stu-id="c1315-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="c1315-106">Se a chamada **QueryInterface** for realizada com sucesso, podemos chamar o método [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) .</span><span class="sxs-lookup"><span data-stu-id="c1315-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="c1315-107">Para essa finalidade, devemos criar um objeto que implementa a interface [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) .</span><span class="sxs-lookup"><span data-stu-id="c1315-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="c1315-108">Passamos essa interface como um parâmetro do método **RegisterSink** .</span><span class="sxs-lookup"><span data-stu-id="c1315-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="c1315-109">O terminal que implementa a chamada [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) armazenará a interface.</span><span class="sxs-lookup"><span data-stu-id="c1315-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="c1315-110">O ponteiro será usado quando o terminal disparar um evento.</span><span class="sxs-lookup"><span data-stu-id="c1315-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="c1315-111">O coletor de eventos pode ter o registro cancelado usando [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span><span class="sxs-lookup"><span data-stu-id="c1315-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
