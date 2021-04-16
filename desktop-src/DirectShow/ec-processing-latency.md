---
description: Indica a quantidade de tempo que um componente está demorando para processar cada exemplo.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d97514b4d2851f619f89f42e644766d50b7d25f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768647"
---
# <a name="ec_processing_latency"></a><span data-ttu-id="92c4a-103">\_latência de processamento do EC \_</span><span class="sxs-lookup"><span data-stu-id="92c4a-103">EC\_PROCESSING\_LATENCY</span></span>

<span data-ttu-id="92c4a-104">Indica a quantidade de tempo que um componente está demorando para processar cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="92c4a-104">Indicates the amount of time that a component is taking to process each sample.</span></span>

## <a name="parameters"></a><span data-ttu-id="92c4a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92c4a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c4a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="92c4a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="92c4a-107">(**\_ tempo de referência const** \* ) a quantidade de tempo para processar cada amostra, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="92c4a-107">(**const REFERENCE\_TIME**\*) The amount of time to process each sample, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="92c4a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="92c4a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="92c4a-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="92c4a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="92c4a-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="92c4a-110">Default Action</span></span>

<span data-ttu-id="92c4a-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="92c4a-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c4a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="92c4a-112">Remarks</span></span>

<span data-ttu-id="92c4a-113">Um apresentador para o filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ) pode enviar essa mensagem para o EVR para notificar o EVR sobre a latência de processamento do apresentador.</span><span class="sxs-lookup"><span data-stu-id="92c4a-113">A presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR to notify the EVR about the presenter's processing latency.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c4a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c4a-114">Requirements</span></span>



| <span data-ttu-id="92c4a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c4a-115">Requirement</span></span> | <span data-ttu-id="92c4a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="92c4a-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92c4a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92c4a-117">Header</span></span><br/> | <dl> <span data-ttu-id="92c4a-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c4a-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c4a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="92c4a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c4a-120">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="92c4a-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="92c4a-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="92c4a-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




