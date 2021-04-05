---
description: Gerado por um coletor de fluxo quando ele conclui a transição para o estado parado. A transição para parada ocorre quando o método IMFPresentationClock Stop é chamado no relógio de apresentação dos coletores.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Evento MEStreamSinkStopped (Mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011340"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="2c06f-104">Evento MEStreamSinkStopped</span><span class="sxs-lookup"><span data-stu-id="2c06f-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="2c06f-105">Gerado por um coletor de fluxo quando ele conclui a transição para o estado parado.</span><span class="sxs-lookup"><span data-stu-id="2c06f-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="2c06f-106">A transição para parada ocorre quando o método [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) é chamado no relógio de apresentação do coletor.</span><span class="sxs-lookup"><span data-stu-id="2c06f-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="2c06f-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="2c06f-107">Event values</span></span>

<span data-ttu-id="2c06f-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="2c06f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2c06f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2c06f-109">VARTYPE</span></span>              | <span data-ttu-id="2c06f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c06f-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2c06f-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="2c06f-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2c06f-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="2c06f-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="2c06f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c06f-113">Requirements</span></span>



| <span data-ttu-id="2c06f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c06f-114">Requirement</span></span> | <span data-ttu-id="2c06f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2c06f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c06f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c06f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c06f-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c06f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c06f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c06f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c06f-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c06f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c06f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c06f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c06f-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c06f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c06f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c06f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c06f-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c06f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="2c06f-124">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="2c06f-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




