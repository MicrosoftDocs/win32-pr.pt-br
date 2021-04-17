---
description: Gerado por um coletor de fluxo quando ele conclui a transição para o estado em pausa.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Evento MEStreamSinkPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811648"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="01dd0-103">Evento MEStreamSinkPaused</span><span class="sxs-lookup"><span data-stu-id="01dd0-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="01dd0-104">Gerado por um coletor de fluxo quando ele conclui a transição para o estado em pausa.</span><span class="sxs-lookup"><span data-stu-id="01dd0-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="01dd0-105">A transição para em pausa ocorre quando o método [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) é chamado no relógio de apresentação do coletor.</span><span class="sxs-lookup"><span data-stu-id="01dd0-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="01dd0-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="01dd0-106">Event values</span></span>

<span data-ttu-id="01dd0-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="01dd0-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="01dd0-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="01dd0-108">VARTYPE</span></span>              | <span data-ttu-id="01dd0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="01dd0-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="01dd0-110">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="01dd0-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="01dd0-111">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="01dd0-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="01dd0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01dd0-112">Requirements</span></span>



| <span data-ttu-id="01dd0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01dd0-113">Requirement</span></span> | <span data-ttu-id="01dd0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="01dd0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01dd0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01dd0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="01dd0-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01dd0-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01dd0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01dd0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="01dd0-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01dd0-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01dd0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01dd0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="01dd0-120"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01dd0-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01dd0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="01dd0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01dd0-122">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01dd0-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="01dd0-123">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="01dd0-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




