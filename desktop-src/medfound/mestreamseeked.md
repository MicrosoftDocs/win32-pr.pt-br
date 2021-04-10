---
description: 'Gerado por um fluxo de mídia após uma chamada para IMFMediaSource:: Start causa uma busca no fluxo. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165036"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="fa252-104">Evento MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="fa252-104">MEStreamSeeked event</span></span>

<span data-ttu-id="fa252-105">Gerado por um fluxo de mídia após uma chamada para [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa uma busca no fluxo.</span><span class="sxs-lookup"><span data-stu-id="fa252-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="fa252-106">Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="fa252-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="fa252-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="fa252-107">Event values</span></span>

<span data-ttu-id="fa252-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="fa252-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fa252-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fa252-109">VARTYPE</span></span>           | <span data-ttu-id="fa252-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa252-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="fa252-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="fa252-111">VT\_I8</span></span><br/> | <span data-ttu-id="fa252-112">Nova hora de início, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="fa252-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="fa252-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa252-113">Requirements</span></span>



| <span data-ttu-id="fa252-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa252-114">Requirement</span></span> | <span data-ttu-id="fa252-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fa252-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa252-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa252-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fa252-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa252-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa252-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa252-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fa252-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa252-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa252-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa252-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa252-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa252-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa252-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa252-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa252-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fa252-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




