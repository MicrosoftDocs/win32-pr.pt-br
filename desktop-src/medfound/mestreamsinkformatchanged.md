---
description: Gerado por um coletor de fluxo quando o tipo de mídia de coletores não é mais válido.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Evento MEStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165035"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="27016-103">Evento MEStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="27016-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="27016-104">Gerado por um coletor de fluxo quando o tipo de mídia do coletor não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="27016-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="27016-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="27016-105">Event values</span></span>

<span data-ttu-id="27016-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="27016-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="27016-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="27016-107">VARTYPE</span></span>              | <span data-ttu-id="27016-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="27016-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="27016-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="27016-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="27016-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="27016-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="27016-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="27016-111">Remarks</span></span>

<span data-ttu-id="27016-112">Um coletor de fluxo pode gerar isso mesmo se algo acontecer invalidando o tipo de mídia do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="27016-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="27016-113">Por exemplo, o processador de vídeo avançado (EVR) envia esse evento quando a exibição é alterada.</span><span class="sxs-lookup"><span data-stu-id="27016-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="27016-114">O valor **HRESULT** recuperado por [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) pode indicar por que o tipo de mídia não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="27016-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="27016-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27016-115">Requirements</span></span>



| <span data-ttu-id="27016-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27016-116">Requirement</span></span> | <span data-ttu-id="27016-117">Valor</span><span class="sxs-lookup"><span data-stu-id="27016-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27016-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27016-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27016-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27016-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27016-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27016-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27016-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27016-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="27016-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27016-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27016-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="27016-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27016-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="27016-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27016-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27016-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="27016-126">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="27016-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




