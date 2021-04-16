---
description: Enviado quando o valor de um SPRM (registro de parâmetro do sistema) é alterado.
ms.assetid: 266b6de1-740d-4b3d-8487-5a9570d6c852
title: EC_DVD_SPRM_Change (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 1af5b8637a197973bca2129a8b8a0198d20248eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750277"
---
# <a name="ec_dvd_sprm_change"></a><span data-ttu-id="ebd48-103">\_Alteração de \_ SPRM de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="ebd48-103">EC\_DVD\_SPRM\_Change</span></span>

<span data-ttu-id="ebd48-104">Enviado quando o valor de um SPRM (registro de parâmetro do sistema) é alterado.</span><span class="sxs-lookup"><span data-stu-id="ebd48-104">Sent when the value of a system parameter register (SPRM) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="ebd48-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ebd48-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebd48-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ebd48-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ebd48-107">O índice de base zero do valor SPRM que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ebd48-107">The zero-based index of the SPRM value that changed.</span></span>

</dd> <dt>

<span data-ttu-id="ebd48-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ebd48-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ebd48-109">Os 16 bits inferiores contêm o novo valor SPRM.</span><span class="sxs-lookup"><span data-stu-id="ebd48-109">The lower 16 bits contains the new SPRM value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ebd48-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebd48-110">Remarks</span></span>

<span data-ttu-id="ebd48-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="ebd48-111">This event is disabled by default.</span></span> <span data-ttu-id="ebd48-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ EnableLoggingEvents** como **true**.</span><span class="sxs-lookup"><span data-stu-id="ebd48-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd48-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd48-113">Requirements</span></span>



| <span data-ttu-id="ebd48-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd48-114">Requirement</span></span> | <span data-ttu-id="ebd48-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ebd48-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd48-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ebd48-116">Header</span></span><br/> | <dl> <span data-ttu-id="ebd48-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ebd48-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd48-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ebd48-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd48-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="ebd48-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ebd48-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="ebd48-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ebd48-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="ebd48-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="ebd48-122">**IDvdInfo2::GetAllSPRMs**</span><span class="sxs-lookup"><span data-stu-id="ebd48-122">**IDvdInfo2::GetAllSPRMs**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)
</dt> </dl>

 

 




