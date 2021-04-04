---
description: Gerado por um coletor de fluxo após o método IMFStreamSink::P laceMarker é chamado.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Evento MEStreamSinkMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661580"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="6b117-103">Evento MEStreamSinkMarker</span><span class="sxs-lookup"><span data-stu-id="6b117-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="6b117-104">Gerado por um coletor de fluxo após o método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) é chamado.</span><span class="sxs-lookup"><span data-stu-id="6b117-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="6b117-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6b117-105">Event values</span></span>

<span data-ttu-id="6b117-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6b117-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6b117-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6b117-107">VARTYPE</span></span>            | <span data-ttu-id="6b117-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b117-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b117-109">>qualquer</span><span class="sxs-lookup"><span data-stu-id="6b117-109">>Any</span></span><br/> | <span data-ttu-id="6b117-110">O valor do evento é uma cópia do **PROPVARIANT** que o chamador especificou no parâmetro *PvarContextValue* do método [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="6b117-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="6b117-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b117-111">Requirements</span></span>



| <span data-ttu-id="6b117-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b117-112">Requirement</span></span> | <span data-ttu-id="6b117-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6b117-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b117-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b117-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b117-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b117-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6b117-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b117-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b117-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6b117-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b117-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b117-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b117-119"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b117-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b117-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b117-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b117-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b117-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="6b117-122">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="6b117-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




