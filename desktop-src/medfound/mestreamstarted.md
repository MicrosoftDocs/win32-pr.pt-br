---
description: Gerado por um fluxo de mídia quando a origem é iniciada sem busca. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765732"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="a9fb2-104">Evento MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="a9fb2-104">MEStreamStarted event</span></span>

<span data-ttu-id="a9fb2-105">Gerado por um fluxo de mídia quando a origem é iniciada sem busca.</span><span class="sxs-lookup"><span data-stu-id="a9fb2-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="a9fb2-106">Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="a9fb2-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="a9fb2-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a9fb2-107">Event values</span></span>

<span data-ttu-id="a9fb2-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a9fb2-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a9fb2-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a9fb2-109">VARTYPE</span></span>              | <span data-ttu-id="a9fb2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9fb2-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fb2-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="a9fb2-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a9fb2-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="a9fb2-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="a9fb2-113">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="a9fb2-113">VT\_I8</span></span><br/>    | <span data-ttu-id="a9fb2-114">A hora de início, em unidades de 100 nanossegundos, em relação aos carimbos de data/hora nos exemplos.</span><span class="sxs-lookup"><span data-stu-id="a9fb2-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a9fb2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9fb2-115">Requirements</span></span>



| <span data-ttu-id="a9fb2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9fb2-116">Requirement</span></span> | <span data-ttu-id="a9fb2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a9fb2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fb2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9fb2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a9fb2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9fb2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a9fb2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9fb2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a9fb2-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9fb2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9fb2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9fb2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9fb2-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9fb2-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9fb2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9fb2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fb2-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9fb2-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




