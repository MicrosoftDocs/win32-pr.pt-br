---
description: Gerado por uma origem de mídia quando ele inicia um novo fluxo.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760991"
---
# <a name="menewstream-event"></a><span data-ttu-id="640cc-103">Evento MENewStream</span><span class="sxs-lookup"><span data-stu-id="640cc-103">MENewStream event</span></span>

<span data-ttu-id="640cc-104">Gerado por uma origem de mídia quando ele inicia um novo fluxo.</span><span class="sxs-lookup"><span data-stu-id="640cc-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="640cc-105">Quando o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) é chamado em uma origem de mídia, a origem da mídia envia um evento para cada fluxo selecionado:</span><span class="sxs-lookup"><span data-stu-id="640cc-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="640cc-106">A origem envia o evento MENewStream se o fluxo não foi selecionado na chamada anterior para [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), ou esta é a primeira chamada para **Iniciar** nesta fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="640cc-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="640cc-107">A origem enviará o evento [MEUpdatedStream](meupdatedstream.md) se o fluxo já tiver sido selecionado na chamada anterior para [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="640cc-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="640cc-108">Nenhum evento é enviado para fluxos não selecionados.</span><span class="sxs-lookup"><span data-stu-id="640cc-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="640cc-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="640cc-109">Event values</span></span>

<span data-ttu-id="640cc-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="640cc-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="640cc-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="640cc-111">VARTYPE</span></span>                | <span data-ttu-id="640cc-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="640cc-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640cc-113">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="640cc-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="640cc-114">Contém um ponteiro para a interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) do fluxo.</span><span class="sxs-lookup"><span data-stu-id="640cc-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="640cc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="640cc-115">Requirements</span></span>



| <span data-ttu-id="640cc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="640cc-116">Requirement</span></span> | <span data-ttu-id="640cc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="640cc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640cc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="640cc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="640cc-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="640cc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="640cc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="640cc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="640cc-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="640cc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="640cc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="640cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="640cc-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="640cc-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640cc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="640cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640cc-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="640cc-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




