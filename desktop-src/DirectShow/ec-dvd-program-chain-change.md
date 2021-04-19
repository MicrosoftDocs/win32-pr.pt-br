---
description: Enviado quando a cadeia de programa atual (PGC) é alterada.
ms.assetid: 80fcd059-6ab4-4116-ac3a-012c451237b3
title: EC_DVD_PROGRAM_CHAIN_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PROGRAM_CHAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: eefd45ac1d147a0409417f215e56a4db490dfdbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757251"
---
# <a name="ec_dvd_program_chain_change"></a><span data-ttu-id="54609-103">\_alteração da \_ cadeia de programas \_ \_ do EC DVD</span><span class="sxs-lookup"><span data-stu-id="54609-103">EC\_DVD\_PROGRAM\_CHAIN\_CHANGE</span></span>

<span data-ttu-id="54609-104">Enviado quando a cadeia de programa atual (PGC) é alterada.</span><span class="sxs-lookup"><span data-stu-id="54609-104">Sent when current program chain (PGC) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="54609-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54609-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54609-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="54609-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="54609-107">O número da nova cadeia de programas (PGCN).</span><span class="sxs-lookup"><span data-stu-id="54609-107">The new program chain number (PGCN).</span></span>

</dd> <dt>

<span data-ttu-id="54609-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="54609-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="54609-109">O LCID (identificador de localidade) do idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="54609-109">The locale identifier (LCID) of the audio language.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54609-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="54609-110">Remarks</span></span>

<span data-ttu-id="54609-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="54609-111">This event is disabled by default.</span></span> <span data-ttu-id="54609-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ NotifyPositionChange** como **true**.</span><span class="sxs-lookup"><span data-stu-id="54609-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54609-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54609-113">Requirements</span></span>



| <span data-ttu-id="54609-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="54609-114">Requirement</span></span> | <span data-ttu-id="54609-115">Valor</span><span class="sxs-lookup"><span data-stu-id="54609-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54609-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54609-116">Header</span></span><br/> | <dl> <span data-ttu-id="54609-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54609-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54609-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="54609-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54609-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="54609-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="54609-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="54609-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="54609-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="54609-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




