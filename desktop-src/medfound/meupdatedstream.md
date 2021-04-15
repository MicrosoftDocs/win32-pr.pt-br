---
description: Gerado por uma origem de mídia quando ele é reiniciado ou busca um fluxo que já está ativo.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506044"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="6e173-103">Evento MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="6e173-103">MEUpdatedStream event</span></span>

<span data-ttu-id="6e173-104">Gerado por uma origem de mídia quando ele é reiniciado ou busca um fluxo que já está ativo.</span><span class="sxs-lookup"><span data-stu-id="6e173-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="6e173-105">Quando o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é chamado em uma origem de mídia, a origem da mídia envia um evento para cada fluxo selecionado:</span><span class="sxs-lookup"><span data-stu-id="6e173-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="6e173-106">A origem envia o evento [MENewStream](menewstream.md) se o fluxo não foi selecionado na chamada anterior para [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou esta é a primeira chamada para **Iniciar** nesta fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="6e173-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="6e173-107">A origem enviará o evento MEUpdatedStream se o fluxo já tiver sido selecionado na chamada anterior para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="6e173-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="6e173-108">Nenhum evento é enviado para fluxos não selecionados.</span><span class="sxs-lookup"><span data-stu-id="6e173-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="6e173-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6e173-109">Event values</span></span>

<span data-ttu-id="6e173-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6e173-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6e173-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6e173-111">VARTYPE</span></span>                | <span data-ttu-id="6e173-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e173-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e173-113">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="6e173-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="6e173-114">Ponteiro para a interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6e173-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6e173-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e173-115">Remarks</span></span>

<span data-ttu-id="6e173-116">Na primeira chamada para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) em que um fluxo se torna ativo, a origem da mídia envia um evento [MENewStream](menewstream.md) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="6e173-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="6e173-117">Em chamadas subsequentes para **Iniciar**, a origem da mídia envia um evento MEUpdatedStream até que o fluxo seja desmarcado.</span><span class="sxs-lookup"><span data-stu-id="6e173-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e173-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e173-118">Requirements</span></span>



| <span data-ttu-id="6e173-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e173-119">Requirement</span></span> | <span data-ttu-id="6e173-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e173-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e173-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e173-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e173-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e173-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6e173-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e173-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e173-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e173-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e173-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e173-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e173-126"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e173-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e173-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e173-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e173-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e173-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




