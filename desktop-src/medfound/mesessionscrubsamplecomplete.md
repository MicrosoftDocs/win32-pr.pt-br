---
description: Gerado pela sessão de mídia quando ele conclui uma solicitação de depuração.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Evento MESessionScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827635"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="e85af-103">Evento MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="e85af-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="e85af-104">Gerado pela sessão de mídia quando ele conclui uma solicitação de depuração.</span><span class="sxs-lookup"><span data-stu-id="e85af-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="e85af-105">A depuração ocorre quando a taxa de reprodução é zero e o aplicativo chama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="e85af-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="e85af-106">Esse evento é gerado depois que cada coletor de fluxo concluiu a solicitação de depuração.</span><span class="sxs-lookup"><span data-stu-id="e85af-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="e85af-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e85af-107">Event values</span></span>

<span data-ttu-id="e85af-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="e85af-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e85af-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e85af-109">VARTYPE</span></span>              | <span data-ttu-id="e85af-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e85af-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e85af-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="e85af-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e85af-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="e85af-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e85af-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e85af-113">Requirements</span></span>



| <span data-ttu-id="e85af-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e85af-114">Requirement</span></span> | <span data-ttu-id="e85af-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e85af-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85af-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e85af-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e85af-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e85af-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e85af-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e85af-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e85af-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e85af-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e85af-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e85af-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e85af-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e85af-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85af-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e85af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85af-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e85af-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e85af-124">MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="e85af-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




