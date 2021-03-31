---
description: Liberando dados
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Liberando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645683"
---
# <a name="flushing-data"></a><span data-ttu-id="f8275-103">Liberando dados</span><span class="sxs-lookup"><span data-stu-id="f8275-103">Flushing Data</span></span>

<span data-ttu-id="f8275-104">O pseudocódigo a seguir mostra como implementar o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :</span><span class="sxs-lookup"><span data-stu-id="f8275-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



<span data-ttu-id="f8275-105">Quando a liberação é iniciada, o método **BeginFlush** pega o bloqueio de filtro, que serializa a alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="f8275-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="f8275-106">Ainda não é seguro pegar o bloqueio de streaming, porque a liberação ocorre no thread do aplicativo, e o thread de streaming pode estar no meio de uma chamada de **recebimento** .</span><span class="sxs-lookup"><span data-stu-id="f8275-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="f8275-107">O PIN precisa garantir que **Receive** não seja bloqueado e que todas as chamadas subseqüentes a serem **recebidas** falharão.</span><span class="sxs-lookup"><span data-stu-id="f8275-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="f8275-108">O método [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) define um sinalizador interno, [**CBaseInputPin:: m \_ bFlushing**](cbaseinputpin-m-bflushing.md).</span><span class="sxs-lookup"><span data-stu-id="f8275-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="f8275-109">Quando o sinalizador for **true**, o método **Receive** falhará.</span><span class="sxs-lookup"><span data-stu-id="f8275-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="f8275-110">Ao entregar o downstream de chamada **BeginFlush** , o PIN garante que todos os filtros downstream liberem suas amostras e retornem de chamadas **Receive** .</span><span class="sxs-lookup"><span data-stu-id="f8275-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="f8275-111">Isso, por sua vez, garante que o PIN de entrada não seja bloqueado aguardando **GetBuffer** ou **Receive**.</span><span class="sxs-lookup"><span data-stu-id="f8275-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="f8275-112">Se o método **Receive** de seu PIN nunca aguardar um evento (por exemplo, para obter recursos), o método **BeginFlush** deverá forçar a espera para terminar definindo o evento.</span><span class="sxs-lookup"><span data-stu-id="f8275-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="f8275-113">Neste ponto, o método **Receive** é garantido para retornar e o sinalizador **m \_ bFlushing** impede que novas chamadas **Receive** façam qualquer trabalho.</span><span class="sxs-lookup"><span data-stu-id="f8275-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="f8275-114">Para alguns filtros, isso é tudo o que o **BeginFlush** precisa fazer.</span><span class="sxs-lookup"><span data-stu-id="f8275-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="f8275-115">O método **EndFlush** sinalizará ao filtro que ele pode começar a receber amostras novamente.</span><span class="sxs-lookup"><span data-stu-id="f8275-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="f8275-116">Outros filtros podem precisar usar variáveis ou recursos em **BeginFlush** que também são usados em **Receive**.</span><span class="sxs-lookup"><span data-stu-id="f8275-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="f8275-117">Nesse caso, o filtro deve manter o bloqueio de streaming primeiro.</span><span class="sxs-lookup"><span data-stu-id="f8275-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="f8275-118">Certifique-se de não fazer isso antes de qualquer uma das etapas anteriores, porque você pode causar um deadlock.</span><span class="sxs-lookup"><span data-stu-id="f8275-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="f8275-119">O método **EndFlush** mantém o bloqueio de filtro e propaga o downstream de chamada:</span><span class="sxs-lookup"><span data-stu-id="f8275-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="f8275-120">O método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) redefine o sinalizador **m \_ bFlushing** como **false**, o que permite que o método **Receive** comece a receber amostras novamente.</span><span class="sxs-lookup"><span data-stu-id="f8275-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="f8275-121">Essa deve ser a última etapa em **EndFlush**, porque o PIN não deve receber amostras até que a liberação esteja concluída e todos os filtros de downstream sejam notificados.</span><span class="sxs-lookup"><span data-stu-id="f8275-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8275-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8275-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8275-123">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="f8275-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



