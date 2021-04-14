---
description: Este tópico descreve como implementar um PIN de visualização em um filtro de captura do DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementando um PIN de visualização (opcional)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370261"
---
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="72c8a-103">Implementando um PIN de visualização (opcional)</span><span class="sxs-lookup"><span data-stu-id="72c8a-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="72c8a-104">Este tópico descreve como implementar um PIN de visualização em um filtro de captura do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="72c8a-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="72c8a-105">Se o filtro tiver um PIN de visualização, o PIN de visualização deverá enviar uma cópia dos dados entregues pelo PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="72c8a-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="72c8a-106">Somente envie dados do PIN de visualização ao fazer isso não fará com que o pino de captura descartar os quadros.</span><span class="sxs-lookup"><span data-stu-id="72c8a-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="72c8a-107">O PIN de captura sempre tem prioridade sobre o PIN de visualização.</span><span class="sxs-lookup"><span data-stu-id="72c8a-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="72c8a-108">O PIN de captura e o pino de visualização devem enviar dados com o mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="72c8a-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="72c8a-109">Portanto, eles devem se conectar usando tipos de mídia idênticos.</span><span class="sxs-lookup"><span data-stu-id="72c8a-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="72c8a-110">Se o PIN de captura se conectar primeiro, o PIN de visualização deverá oferecer o mesmo tipo de mídia e rejeitar outros tipos.</span><span class="sxs-lookup"><span data-stu-id="72c8a-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="72c8a-111">Se o pino de visualização se conectar primeiro e o PIN de captura se conectar com um tipo de mídia diferente, o PIN de visualização deverá se reconectar usando o novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="72c8a-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="72c8a-112">Se o filtro downstream do PIN de visualização rejeitar o novo tipo, o PIN de captura também deverá rejeitar o tipo.</span><span class="sxs-lookup"><span data-stu-id="72c8a-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="72c8a-113">Use o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) para consultar o downstream de filtro do PIN de visualização e use o método [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) para reconectar o PIN.</span><span class="sxs-lookup"><span data-stu-id="72c8a-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="72c8a-114">Essas regras também se aplicam se o Gerenciador do grafo de filtro reconectar o PIN de captura.</span><span class="sxs-lookup"><span data-stu-id="72c8a-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="72c8a-115">O exemplo a seguir mostra um contorno desse processo:</span><span class="sxs-lookup"><span data-stu-id="72c8a-115">The following example shows an outline of this process:</span></span>


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a><span data-ttu-id="72c8a-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72c8a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72c8a-117">Como os filtros se conectam</span><span class="sxs-lookup"><span data-stu-id="72c8a-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="72c8a-118">Gravando filtros de captura</span><span class="sxs-lookup"><span data-stu-id="72c8a-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



