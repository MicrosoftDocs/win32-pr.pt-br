---
description: Gerado por um coletor de fluxo quando ele conclui a transição para o estado de execução.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Evento MEStreamSinkStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798049"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="40c7c-103">Evento MEStreamSinkStarted</span><span class="sxs-lookup"><span data-stu-id="40c7c-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="40c7c-104">Gerado por um coletor de fluxo quando ele conclui a transição para o estado de execução.</span><span class="sxs-lookup"><span data-stu-id="40c7c-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="40c7c-105">A transição para a execução ocorre quando o método [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) é chamado no relógio de apresentação do coletor.</span><span class="sxs-lookup"><span data-stu-id="40c7c-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="40c7c-106">O coletor de mídia recebe a notificação por meio de seu método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou [**IMFClockStateSink:: OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .</span><span class="sxs-lookup"><span data-stu-id="40c7c-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="40c7c-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="40c7c-107">Event values</span></span>

<span data-ttu-id="40c7c-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="40c7c-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="40c7c-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="40c7c-109">VARTYPE</span></span>              | <span data-ttu-id="40c7c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="40c7c-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="40c7c-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="40c7c-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="40c7c-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="40c7c-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="40c7c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40c7c-113">Requirements</span></span>



| <span data-ttu-id="40c7c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="40c7c-114">Requirement</span></span> | <span data-ttu-id="40c7c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="40c7c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c7c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c7c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="40c7c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40c7c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="40c7c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40c7c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="40c7c-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40c7c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="40c7c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40c7c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c7c-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40c7c-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c7c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="40c7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c7c-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="40c7c-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="40c7c-124">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="40c7c-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




