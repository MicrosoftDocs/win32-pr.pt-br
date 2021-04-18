---
description: Sinaliza o final de qualquer ainda (PGC, Cell ou VOBU).
ms.assetid: 459464b1-3085-4ad7-8eb3-960cee89d395
title: EC_DVD_STILL_OFF (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_OFF
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 811bc85deafb40676041280daa0a1cdd8f8b3dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812781"
---
# <a name="ec_dvd_still_off"></a><span data-ttu-id="0071c-103">o \_ DVD do EC \_ ainda está \_ desativado</span><span class="sxs-lookup"><span data-stu-id="0071c-103">EC\_DVD\_STILL\_OFF</span></span>

<span data-ttu-id="0071c-104">Sinaliza o final de qualquer ainda (PGC, Cell ou VOBU).</span><span class="sxs-lookup"><span data-stu-id="0071c-104">Signals the end of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="0071c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0071c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0071c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0071c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0071c-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="0071c-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="0071c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0071c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0071c-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="0071c-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0071c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0071c-110">Remarks</span></span>

<span data-ttu-id="0071c-111">Esse evento indica que qualquer um atualmente ativo ainda foi lançado.</span><span class="sxs-lookup"><span data-stu-id="0071c-111">This event indicates that any currently active still has been released.</span></span>

<span data-ttu-id="0071c-112">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="0071c-112">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="0071c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0071c-113">Requirements</span></span>



| <span data-ttu-id="0071c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0071c-114">Requirement</span></span> | <span data-ttu-id="0071c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0071c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0071c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0071c-116">Header</span></span><br/> | <dl> <span data-ttu-id="0071c-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0071c-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0071c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0071c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0071c-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="0071c-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="0071c-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="0071c-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0071c-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="0071c-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




