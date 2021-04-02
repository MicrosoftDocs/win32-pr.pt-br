---
description: Gerado por uma fonte de mídia que fornece topologias por meio da interface IMFMediaSourceTopologyProvider, como a origem do sequenciador. A origem gera o evento quando ele tem uma nova apresentação. A sessão de mídia encaminha esse evento para o aplicativo.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Evento MENewPresentation (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165045"
---
# <a name="menewpresentation-event"></a><span data-ttu-id="13d23-105">Evento MENewPresentation</span><span class="sxs-lookup"><span data-stu-id="13d23-105">MENewPresentation event</span></span>

<span data-ttu-id="13d23-106">Gerado por uma fonte de mídia que fornece topologias por meio da interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , como a origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="13d23-106">Raised by a media source that provides topologies through the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface, such as the sequencer source.</span></span> <span data-ttu-id="13d23-107">A origem gera o evento quando ele tem uma nova apresentação.</span><span class="sxs-lookup"><span data-stu-id="13d23-107">The source raises the event when it has a new presentation.</span></span> <span data-ttu-id="13d23-108">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13d23-108">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="13d23-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="13d23-109">Event values</span></span>

<span data-ttu-id="13d23-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="13d23-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="13d23-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="13d23-111">VARTYPE</span></span>                | <span data-ttu-id="13d23-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="13d23-112">Description</span></span>                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d23-113">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="13d23-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="13d23-114">Ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação da nova apresentação.</span><span class="sxs-lookup"><span data-stu-id="13d23-114">Pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor for the new presentation.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="13d23-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d23-115">Remarks</span></span>

<span data-ttu-id="13d23-116">O aplicativo pode obter a topologia que corresponde ao descritor de apresentação chamando [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="13d23-116">The application can get the topology that corresponds to the presentation descriptor by calling [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the media source.</span></span> <span data-ttu-id="13d23-117">O aplicativo pode então enfileirar a nova topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="13d23-117">The application can then queue the new topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

## <a name="requirements"></a><span data-ttu-id="13d23-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d23-118">Requirements</span></span>



| <span data-ttu-id="13d23-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d23-119">Requirement</span></span> | <span data-ttu-id="13d23-120">Valor</span><span class="sxs-lookup"><span data-stu-id="13d23-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d23-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d23-121">Minimum supported client</span></span><br/> | <span data-ttu-id="13d23-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13d23-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13d23-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d23-123">Minimum supported server</span></span><br/> | <span data-ttu-id="13d23-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13d23-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13d23-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13d23-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="13d23-126"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13d23-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d23-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="13d23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d23-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13d23-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="13d23-129">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="13d23-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




