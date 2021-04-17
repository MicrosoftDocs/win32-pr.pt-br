---
description: O grafo está descartando amostras, para controle de qualidade.
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: EC_QUALITY_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5752db30c8ad6ed85655948cf2adb9ef7ac8078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789952"
---
# <a name="ec_quality_change"></a><span data-ttu-id="e2d1b-103">\_alteração de qualidade do EC \_</span><span class="sxs-lookup"><span data-stu-id="e2d1b-103">EC\_QUALITY\_CHANGE</span></span>

<span data-ttu-id="e2d1b-104">O grafo está descartando amostras, para controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2d1b-104">The graph is dropping samples, for quality control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2d1b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2d1b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d1b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e2d1b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e2d1b-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="e2d1b-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2d1b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e2d1b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e2d1b-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="e2d1b-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="e2d1b-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="e2d1b-110">Default Action</span></span>

<span data-ttu-id="e2d1b-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e2d1b-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d1b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2d1b-112">Remarks</span></span>

<span data-ttu-id="e2d1b-113">Um filtro enviará esse evento se ele soltar amostras em resposta a uma mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2d1b-113">A filter sends this event if it drops samples in response to a quality control message.</span></span> <span data-ttu-id="e2d1b-114">Ele envia o evento somente quando ele ajusta o nível de qualidade, e não para cada amostra que ele descarta.</span><span class="sxs-lookup"><span data-stu-id="e2d1b-114">It sends the event only when it adjusts the quality level, not for each sample that it drops.</span></span> <span data-ttu-id="e2d1b-115">Para obter mais informações, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="e2d1b-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d1b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d1b-116">Requirements</span></span>



| <span data-ttu-id="e2d1b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d1b-117">Requirement</span></span> | <span data-ttu-id="e2d1b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e2d1b-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d1b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2d1b-119">Header</span></span><br/> | <dl> <span data-ttu-id="e2d1b-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2d1b-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d1b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2d1b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d1b-122">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="e2d1b-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e2d1b-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="e2d1b-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




