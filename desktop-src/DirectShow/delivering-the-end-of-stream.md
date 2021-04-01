---
description: Entregando o fim do fluxo
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Entregando o fim do fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825551"
---
# <a name="delivering-the-end-of-stream"></a><span data-ttu-id="41970-103">Entregando o fim do fluxo</span><span class="sxs-lookup"><span data-stu-id="41970-103">Delivering the End of Stream</span></span>

<span data-ttu-id="41970-104">Quando o PIN de entrada recebe uma notificação de fim de fluxo, ele propaga a chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="41970-104">When the input pin receives an end-of-stream notification, it propagates the call downstream.</span></span> <span data-ttu-id="41970-105">Todos os filtros downstream que recebem dados desse PIN de entrada também devem obter a notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="41970-105">Any downstream filters that receive data from this input pin should also get the end-of-stream notification.</span></span> <span data-ttu-id="41970-106">Novamente, faça o bloqueio de streaming e não o bloqueio de filtro.</span><span class="sxs-lookup"><span data-stu-id="41970-106">Again, take the streaming lock and not the filter lock.</span></span> <span data-ttu-id="41970-107">Se o filtro tiver dados pendentes que ainda não foram entregues, o filtro deverá entregá-lo agora, antes de enviar a notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="41970-107">If the filter has pending data that was not yet delivered, the filter should deliver it now, before it sends the end-of-stream notification.</span></span> <span data-ttu-id="41970-108">Ele não deve enviar dados após o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="41970-108">It should not send any data after the end of the stream.</span></span>


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



<span data-ttu-id="41970-109">O método [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) chama [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="41970-109">The [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method calls [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41970-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="41970-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41970-111">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="41970-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



