---
description: Enviado quando o número do programa de DVD ou o número da célula é alterado.
ms.assetid: a500e86d-cd42-4716-9c57-828a72c4e1df
title: EC_DVD_PROGRAM_CELL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CELL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: d41f691016c3e41cfc3e14ed1ce6fff276dcc70e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752275"
---
# <a name="ec_dvd_program_cell_change"></a><span data-ttu-id="619d6-103">\_alteração de \_ célula do programa de DVD do EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="619d6-103">EC\_DVD\_PROGRAM\_CELL\_CHANGE</span></span>

<span data-ttu-id="619d6-104">Enviado quando o número do programa de DVD ou o número da célula é alterado.</span><span class="sxs-lookup"><span data-stu-id="619d6-104">Sent when the DVD program number or cell number changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="619d6-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="619d6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619d6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="619d6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="619d6-107">O número do novo programa.</span><span class="sxs-lookup"><span data-stu-id="619d6-107">The new program number.</span></span>

</dd> <dt>

<span data-ttu-id="619d6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="619d6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="619d6-109">O novo número de célula.</span><span class="sxs-lookup"><span data-stu-id="619d6-109">The new cell number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="619d6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="619d6-110">Remarks</span></span>

<span data-ttu-id="619d6-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="619d6-111">This event is disabled by default.</span></span> <span data-ttu-id="619d6-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ NotifyPositionChange** como **true**.</span><span class="sxs-lookup"><span data-stu-id="619d6-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="619d6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="619d6-113">Requirements</span></span>



| <span data-ttu-id="619d6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="619d6-114">Requirement</span></span> | <span data-ttu-id="619d6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="619d6-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619d6-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="619d6-116">Header</span></span><br/> | <dl> <span data-ttu-id="619d6-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="619d6-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="619d6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="619d6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619d6-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="619d6-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="619d6-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="619d6-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="619d6-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="619d6-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




