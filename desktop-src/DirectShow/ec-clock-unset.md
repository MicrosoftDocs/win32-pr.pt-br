---
description: O provedor de relógio foi desconectado.
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: EC_CLOCK_UNSET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ead35d89eee94bbffb38a96f658ccb2bb6e6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766314"
---
# <a name="ec_clock_unset"></a><span data-ttu-id="805a3-103">desdefinição do relógio do EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="805a3-103">EC\_CLOCK\_UNSET</span></span>

<span data-ttu-id="805a3-104">O provedor de relógio foi desconectado.</span><span class="sxs-lookup"><span data-stu-id="805a3-104">The clock provider was disconnected.</span></span>

## <a name="parameters"></a><span data-ttu-id="805a3-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="805a3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805a3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="805a3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="805a3-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="805a3-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="805a3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="805a3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="805a3-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="805a3-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="805a3-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="805a3-110">Default Action</span></span>

<span data-ttu-id="805a3-111">O Gerenciador de gráfico de filtro escolhe um novo relógio de referência no próximo comando Pause ou Run.</span><span class="sxs-lookup"><span data-stu-id="805a3-111">The Filter Graph Manager chooses a new reference clock on the next pause or run command.</span></span> <span data-ttu-id="805a3-112">Ele também encaminha o evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="805a3-112">It also forwards the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="805a3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="805a3-113">Remarks</span></span>

<span data-ttu-id="805a3-114">KSProxy sinaliza esse evento quando o PIN de um filtro que fornece um relógio é desconectado.</span><span class="sxs-lookup"><span data-stu-id="805a3-114">KSProxy signals this event when the pin of a clock-providing filter is disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="805a3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805a3-115">Requirements</span></span>



| <span data-ttu-id="805a3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="805a3-116">Requirement</span></span> | <span data-ttu-id="805a3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="805a3-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="805a3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="805a3-118">Header</span></span><br/> | <dl> <span data-ttu-id="805a3-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="805a3-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805a3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="805a3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805a3-121">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="805a3-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="805a3-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="805a3-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




