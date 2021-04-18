---
description: Indica o novo domínio do DVD Player.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 815b6b2dd318d0b7716f4cf640ef3f83dacd0d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751878"
---
# <a name="ec_dvd_domain_change"></a><span data-ttu-id="214f3-103">\_alteração de \_ domínio de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="214f3-103">EC\_DVD\_DOMAIN\_CHANGE</span></span>

<span data-ttu-id="214f3-104">Indica o novo domínio do DVD Player.</span><span class="sxs-lookup"><span data-stu-id="214f3-104">Indicates the DVD player's new domain.</span></span>

## <a name="parameters"></a><span data-ttu-id="214f3-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="214f3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="214f3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="214f3-107">Valor **DWORD** que indica o novo domínio.</span><span class="sxs-lookup"><span data-stu-id="214f3-107">**DWORD** value indicating the new domain.</span></span> <span data-ttu-id="214f3-108">Membro do tipo de dados enumerado de [**\_ domínio de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_domain) .</span><span class="sxs-lookup"><span data-stu-id="214f3-108">Member of the [**DVD\_DOMAIN**](/windows/win32/api/strmif/ne-strmif-dvd_domain) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="214f3-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="214f3-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="214f3-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="214f3-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="214f3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="214f3-111">Remarks</span></span>

<span data-ttu-id="214f3-112">O DVD Player sinaliza esse evento sempre que ele altera domínios.</span><span class="sxs-lookup"><span data-stu-id="214f3-112">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="214f3-113">Esse evento é gerado em todos os domínios de DVD.</span><span class="sxs-lookup"><span data-stu-id="214f3-113">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="214f3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214f3-114">Requirements</span></span>



| <span data-ttu-id="214f3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="214f3-115">Requirement</span></span> | <span data-ttu-id="214f3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="214f3-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="214f3-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="214f3-117">Header</span></span><br/> | <dl> <span data-ttu-id="214f3-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="214f3-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214f3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="214f3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214f3-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="214f3-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="214f3-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="214f3-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="214f3-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="214f3-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




