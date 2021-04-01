---
description: 'Gerado depois que o método IMFMediaSession:: settopology é concluído de forma assíncrona. A sessão de mídia gera esse evento depois que resolve a topologia em uma topologia completa e enfileira a topologia para reprodução.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921281"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="cabc3-104">Evento MESessionTopologySet</span><span class="sxs-lookup"><span data-stu-id="cabc3-104">MESessionTopologySet event</span></span>

<span data-ttu-id="cabc3-105">Gerado depois que o método [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="cabc3-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="cabc3-106">A sessão de mídia gera esse evento depois que resolve a topologia em uma topologia completa e enfileira a topologia para reprodução.</span><span class="sxs-lookup"><span data-stu-id="cabc3-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="cabc3-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="cabc3-107">Event values</span></span>

<span data-ttu-id="cabc3-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="cabc3-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="cabc3-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="cabc3-109">VARTYPE</span></span>                | <span data-ttu-id="cabc3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="cabc3-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cabc3-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="cabc3-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="cabc3-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="cabc3-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="cabc3-113">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="cabc3-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="cabc3-114">Ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia completa.</span><span class="sxs-lookup"><span data-stu-id="cabc3-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="cabc3-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cabc3-115">Examples</span></span>

<span data-ttu-id="cabc3-116">O exemplo a seguir recupera o ponteiro [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de um evento MESessionTopologySet.</span><span class="sxs-lookup"><span data-stu-id="cabc3-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="cabc3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cabc3-117">Requirements</span></span>



| <span data-ttu-id="cabc3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cabc3-118">Requirement</span></span> | <span data-ttu-id="cabc3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cabc3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cabc3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cabc3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cabc3-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cabc3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cabc3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cabc3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cabc3-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cabc3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cabc3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cabc3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cabc3-125"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cabc3-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cabc3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cabc3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cabc3-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cabc3-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




