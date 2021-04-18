---
description: Gerado por um fluxo de mídia quando o método IMFMediaSource::P ause é concluído de forma assíncrona.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Evento MEStreamPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793397"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="8452c-103">Evento MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="8452c-103">MEStreamPaused event</span></span>

<span data-ttu-id="8452c-104">Gerado por um fluxo de mídia quando o método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8452c-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="8452c-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="8452c-105">Event values</span></span>

<span data-ttu-id="8452c-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="8452c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8452c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8452c-107">VARTYPE</span></span>              | <span data-ttu-id="8452c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8452c-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="8452c-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="8452c-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="8452c-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="8452c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8452c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8452c-111">Remarks</span></span>

<span data-ttu-id="8452c-112">Cada fluxo ativo na apresentação envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="8452c-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8452c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8452c-113">Requirements</span></span>



| <span data-ttu-id="8452c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8452c-114">Requirement</span></span> | <span data-ttu-id="8452c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8452c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8452c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8452c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8452c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8452c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8452c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8452c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8452c-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8452c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8452c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8452c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8452c-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8452c-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8452c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8452c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8452c-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8452c-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




