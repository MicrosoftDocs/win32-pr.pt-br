---
description: 'Gerado quando uma fonte de mídia busca uma nova posição. Uma fonte de mídia gerará esse evento se a fonte estiver em execução ou em pausa e o aplicativo chamar IMFMediaSource:: Start com uma hora de início que não seja igual à posição atual.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762503"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="64ba5-104">Evento MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="64ba5-104">MESourceSeeked event</span></span>

<span data-ttu-id="64ba5-105">Gerado quando uma fonte de mídia busca uma nova posição.</span><span class="sxs-lookup"><span data-stu-id="64ba5-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="64ba5-106">Uma fonte de mídia gerará esse evento se a fonte estiver em execução ou em pausa e o aplicativo chamar [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) com uma hora de início que não seja igual à posição atual.</span><span class="sxs-lookup"><span data-stu-id="64ba5-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="64ba5-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="64ba5-107">Event values</span></span>

<span data-ttu-id="64ba5-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="64ba5-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="64ba5-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="64ba5-109">VARTYPE</span></span>           | <span data-ttu-id="64ba5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="64ba5-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="64ba5-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="64ba5-111">VT\_I8</span></span><br/> | <span data-ttu-id="64ba5-112">A nova posição inicial, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="64ba5-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="64ba5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64ba5-113">Requirements</span></span>



| <span data-ttu-id="64ba5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="64ba5-114">Requirement</span></span> | <span data-ttu-id="64ba5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="64ba5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ba5-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64ba5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="64ba5-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64ba5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64ba5-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64ba5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="64ba5-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="64ba5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64ba5-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64ba5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="64ba5-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64ba5-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ba5-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="64ba5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ba5-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64ba5-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




