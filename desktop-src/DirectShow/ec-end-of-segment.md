---
description: O fim de um segmento foi atingido.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757250"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="a51f3-103">\_fim \_ do \_ segmento do EC</span><span class="sxs-lookup"><span data-stu-id="a51f3-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="a51f3-104">O fim de um segmento foi atingido.</span><span class="sxs-lookup"><span data-stu-id="a51f3-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="a51f3-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a51f3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a51f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a51f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a51f3-107">( **\_ tempo de referência** const \* ) ponteiro para um valor de **\_ tempo de referência** que especifica o tempo de fluxo acumulado desde o início do segmento, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="a51f3-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a51f3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a51f3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a51f3-109">(**DWORD**) Número do segmento (baseado em zero).</span><span class="sxs-lookup"><span data-stu-id="a51f3-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a51f3-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="a51f3-110">Default Action</span></span>

<span data-ttu-id="a51f3-111">O Gerenciador de gráfico de filtro verifica o número de eventos de **\_ fim \_ de \_ segmento do EC** em relação ao número de eventos de [**segmento do EC \_ \_ iniciados**](ec-segment-started.md) .</span><span class="sxs-lookup"><span data-stu-id="a51f3-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="a51f3-112">Se eles corresponderem, ele encaminha **o \_ fim \_ do evento de \_ segmento do EC** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a51f3-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="a51f3-113">Os aplicativos não podem substituir a ação padrão para este evento.</span><span class="sxs-lookup"><span data-stu-id="a51f3-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="a51f3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a51f3-114">Remarks</span></span>

<span data-ttu-id="a51f3-115">Esse código de evento dá suporte a loop contínuo.</span><span class="sxs-lookup"><span data-stu-id="a51f3-115">This event code supports seamless looping.</span></span> <span data-ttu-id="a51f3-116">Quando uma chamada para o método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) inclui o \_ sinalizador de segmento de busca \_ , o filtro de origem envia esse código de evento em vez de chamar [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span><span class="sxs-lookup"><span data-stu-id="a51f3-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="a51f3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a51f3-117">Requirements</span></span>



| <span data-ttu-id="a51f3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a51f3-118">Requirement</span></span> | <span data-ttu-id="a51f3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a51f3-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a51f3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a51f3-120">Header</span></span><br/> | <dl> <span data-ttu-id="a51f3-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a51f3-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a51f3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a51f3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51f3-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="a51f3-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a51f3-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="a51f3-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




