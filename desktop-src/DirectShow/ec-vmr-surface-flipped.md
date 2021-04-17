---
description: Enviado quando o apresentador de alocador VMR-7's chamou o método flip do DirectDraw na superfície apresentada. Isso permite que o VMR mantenha sua tabela DirectXVA de superfícies sincronizadas com a cadeia de inversão do DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749005"
---
# <a name="ec_vmr_surface_flipped"></a><span data-ttu-id="e429d-104">superfície do EC \_ VMR \_ \_ invertida</span><span class="sxs-lookup"><span data-stu-id="e429d-104">EC\_VMR\_SURFACE\_FLIPPED</span></span>

<span data-ttu-id="e429d-105">Enviado quando o apresentador de alocador VMR-7's chamou o método flip do DirectDraw na superfície apresentada.</span><span class="sxs-lookup"><span data-stu-id="e429d-105">Sent when the VMR-7's allocator presenter has called the DirectDraw Flip method on the surface being presented.</span></span> <span data-ttu-id="e429d-106">Isso permite que o VMR mantenha sua tabela DirectXVA de superfícies sincronizadas com a cadeia de inversão do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="e429d-106">This allows the VMR to keep its DirectXVA table of surfaces synchronized with DirectDraw's flipping chain.</span></span>

## <a name="parameters"></a><span data-ttu-id="e429d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e429d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e429d-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e429d-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e429d-109">(**HRESULT**) Código de status retornado do método flip do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="e429d-109">(**HRESULT**) Status code returned from the DirectDraw Flip method.</span></span>

</dd> <dt>

<span data-ttu-id="e429d-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e429d-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e429d-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="e429d-111">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e429d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e429d-112">Remarks</span></span>

<span data-ttu-id="e429d-113">Alocador personalizado-os apresentadores para o VMR-7 devem enviar esse evento.</span><span class="sxs-lookup"><span data-stu-id="e429d-113">Custom allocator-presenters for the VMR-7 should send this event.</span></span> <span data-ttu-id="e429d-114">Este evento não é encaminhado para aplicativos e não é usado com os apresentadores de alocador para o VMR-9.</span><span class="sxs-lookup"><span data-stu-id="e429d-114">This event is not forwarded to applications and it is not used with allocator-presenters for the VMR-9.</span></span>

## <a name="requirements"></a><span data-ttu-id="e429d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e429d-115">Requirements</span></span>



| <span data-ttu-id="e429d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e429d-116">Requirement</span></span> | <span data-ttu-id="e429d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e429d-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e429d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e429d-118">Header</span></span><br/> | <dl> <span data-ttu-id="e429d-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e429d-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e429d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e429d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e429d-121">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="e429d-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e429d-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="e429d-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




