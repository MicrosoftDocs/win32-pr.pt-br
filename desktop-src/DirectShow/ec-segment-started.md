---
description: Um novo segmento foi iniciado.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751232"
---
# <a name="ec_segment_started"></a><span data-ttu-id="c04e2-103">segmento de EC \_ \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="c04e2-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="c04e2-104">Um novo segmento foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="c04e2-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="c04e2-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c04e2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c04e2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c04e2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c04e2-107">( **\_ tempo de referência** const \* ) ponteiro para um valor de **\_ tempo de referência** que especifica o tempo de fluxo acumulado desde o início do segmento, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="c04e2-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="c04e2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c04e2-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c04e2-109">(**DWORD**) Número do segmento (baseado em zero).</span><span class="sxs-lookup"><span data-stu-id="c04e2-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="c04e2-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="c04e2-110">Default Action</span></span>

<span data-ttu-id="c04e2-111">Esse evento não é enviado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c04e2-111">This event is not sent to the application.</span></span> <span data-ttu-id="c04e2-112">Os aplicativos não podem substituir a ação padrão para este evento.</span><span class="sxs-lookup"><span data-stu-id="c04e2-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="c04e2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c04e2-113">Remarks</span></span>

<span data-ttu-id="c04e2-114">Se um filtro enviar um [**\_ fim \_ de \_ segmento do EC**](ec-end-of-segment.md) no final de um segmento, ele enviará esse evento no início do segmento.</span><span class="sxs-lookup"><span data-stu-id="c04e2-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="c04e2-115">O Gerenciador do grafo de filtro usa essa notificação de evento para calcular quantas \_ \_ notificações de fim de segmento do EC \_ devem esperar no final do segmento.</span><span class="sxs-lookup"><span data-stu-id="c04e2-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="c04e2-116">Por padrão, os filtros não enviam eventos [**\_ \_ de fim de \_ segmento do EC**](ec-end-of-segment.md) no final dos segmentos e, portanto, não devem enviar esse evento.</span><span class="sxs-lookup"><span data-stu-id="c04e2-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="c04e2-117">Para obter mais informações, consulte [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="c04e2-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="c04e2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c04e2-118">Requirements</span></span>



| <span data-ttu-id="c04e2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c04e2-119">Requirement</span></span> | <span data-ttu-id="c04e2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c04e2-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c04e2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c04e2-121">Header</span></span><br/> | <dl> <span data-ttu-id="c04e2-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="c04e2-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c04e2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c04e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04e2-124">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="c04e2-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c04e2-125">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="c04e2-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




