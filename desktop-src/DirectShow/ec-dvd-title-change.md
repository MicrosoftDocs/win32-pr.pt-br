---
description: Indica quando o número de título do DVD atual é alterado.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751233"
---
# <a name="ec_dvd_title_change"></a><span data-ttu-id="f3d4f-103">\_alteração do \_ título do DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="f3d4f-103">EC\_DVD\_TITLE\_CHANGE</span></span>

<span data-ttu-id="f3d4f-104">Indica quando o número de título do DVD atual é alterado.</span><span class="sxs-lookup"><span data-stu-id="f3d4f-104">Indicates when the current DVD title number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3d4f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3d4f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3d4f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f3d4f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f3d4f-107">Valor **DWORD** que indica o novo número de título.</span><span class="sxs-lookup"><span data-stu-id="f3d4f-107">**DWORD** value indicating the new title number.</span></span>

</dd> <dt>

<span data-ttu-id="f3d4f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f3d4f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f3d4f-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="f3d4f-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3d4f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3d4f-110">Remarks</span></span>

<span data-ttu-id="f3d4f-111">Os números de título variam de 1 a 99.</span><span class="sxs-lookup"><span data-stu-id="f3d4f-111">Title numbers range from 1 to 99.</span></span> <span data-ttu-id="f3d4f-112">Esse número indica o TTN, que é o número de título em relação ao disco inteiro, e não VTS \_ TTN, que é o número de título em relação a apenas uma VTS atual.</span><span class="sxs-lookup"><span data-stu-id="f3d4f-112">This number indicates the TTN, which is the title number with respect to the whole disc, not the VTS\_TTN which is the title number with respect to just a current VTS.</span></span>

<span data-ttu-id="f3d4f-113">Esse evento é gerado no domínio do título.</span><span class="sxs-lookup"><span data-stu-id="f3d4f-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d4f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3d4f-114">Requirements</span></span>



| <span data-ttu-id="f3d4f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3d4f-115">Requirement</span></span> | <span data-ttu-id="f3d4f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f3d4f-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d4f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3d4f-117">Header</span></span><br/> | <dl> <span data-ttu-id="f3d4f-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3d4f-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3d4f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3d4f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d4f-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="f3d4f-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f3d4f-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="f3d4f-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f3d4f-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3d4f-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




