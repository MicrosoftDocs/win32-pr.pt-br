---
description: Recebendo e entregando exemplos
ms.assetid: 92954b40-1424-4dee-997c-fc41089b7fa5
title: Recebendo e entregando exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364743e0dfc201d419a61fa4c88bde686976d6b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825699"
---
# <a name="receiving-and-delivering-samples"></a><span data-ttu-id="22697-103">Recebendo e entregando exemplos</span><span class="sxs-lookup"><span data-stu-id="22697-103">Receiving and Delivering Samples</span></span>

<span data-ttu-id="22697-104">O pseudocódigo a seguir mostra como implementar o método **IMemInput:: Receive** :</span><span class="sxs-lookup"><span data-stu-id="22697-104">The following pseudocode shows how to implement the **IMemInput::Receive** method:</span></span>


```C++
HRESULT CMyInputPin::Receive(IMediaSample *pSample)
{
    CAutoLock cObjectLock(&m_csReceive);

    // Perhaps the filter needs to wait on something.
    WaitForSingleObject(m_hSomeEventThatReceiveNeedsToWaitOn, INFINITE);

    // Before using resources, make sure it is safe to proceed. Do not
    // continue if the base-class method returns anything besides S_OK.
    hr = CBaseInputPin::Receive(pSample);
    if (hr != S_OK) 
    {
        return hr;
    }

    /* It is safe to use resources allocated in Active and Pause. */

    // Deliver sample(s), via your output pin(s).
    for (each output pin)
        pOutputPin->Deliver(pSample);

    return hr;
}
```



<span data-ttu-id="22697-105">O método **Receive** mantém o bloqueio de streaming, não o bloqueio de filtro.</span><span class="sxs-lookup"><span data-stu-id="22697-105">The **Receive** method holds the streaming lock, not the filter lock.</span></span> <span data-ttu-id="22697-106">O filtro pode precisar aguardar algum evento antes de poder processar os dados, mostrados aqui pela chamada para **WaitForSingleObject**.</span><span class="sxs-lookup"><span data-stu-id="22697-106">The filter might need to wait on some event before it can process the data, shown here by the call to **WaitForSingleObject**.</span></span> <span data-ttu-id="22697-107">Nem todo filtro precisará fazer isso.</span><span class="sxs-lookup"><span data-stu-id="22697-107">Not every filter will need to do this.</span></span> <span data-ttu-id="22697-108">O método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) verifica algumas condições gerais de streaming.</span><span class="sxs-lookup"><span data-stu-id="22697-108">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method verifies some general streaming conditions.</span></span> <span data-ttu-id="22697-109">Ele retornará o \_ estado VFW E \_ incorreto \_ se o filtro for interrompido, S \_ false se o filtro estiver sendo liberado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="22697-109">It returns VFW\_E\_WRONG\_STATE if the filter is stopped, S\_FALSE if the filter is flushing, and so forth.</span></span> <span data-ttu-id="22697-110">Qualquer código de retorno diferente de S \_ OK indica que o método **Receive** deve retornar imediatamente e não processar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="22697-110">Any return code other than S\_OK indicates that the **Receive** method should return immediately and not process the sample.</span></span>

<span data-ttu-id="22697-111">Depois que o exemplo for processado, entregue-o ao filtro downstream chamando [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md).</span><span class="sxs-lookup"><span data-stu-id="22697-111">After the sample is processed, deliver it to the downstream filter by calling [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md).</span></span> <span data-ttu-id="22697-112">Esse método auxiliar chama **IMemInputPin:: Receive** no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="22697-112">This helper method calls **IMemInputPin::Receive** on the downstream input pin.</span></span> <span data-ttu-id="22697-113">Um filtro pode fornecer amostras para vários Pins.</span><span class="sxs-lookup"><span data-stu-id="22697-113">A filter might deliver samples to several pins.</span></span>

 

 



