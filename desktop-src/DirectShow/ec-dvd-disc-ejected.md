---
description: Sinaliza que um disco DVD foi ejetado.
ms.assetid: 031156c2-f0f0-4a9e-b792-4d656ec49aef
title: EC_DVD_DISC_EJECTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_EJECTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: ab6c1333245b589d4f13bafcba89eada3ef98ab0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747802"
---
# <a name="ec_dvd_disc_ejected"></a><span data-ttu-id="3fdcf-103">\_disco DVD do EC \_ \_ ejetado</span><span class="sxs-lookup"><span data-stu-id="3fdcf-103">EC\_DVD\_DISC\_EJECTED</span></span>

<span data-ttu-id="3fdcf-104">Sinaliza que um disco DVD foi ejetado.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-104">Signals that a DVD disc was ejected.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fdcf-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fdcf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fdcf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3fdcf-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3fdcf-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="3fdcf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3fdcf-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3fdcf-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fdcf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fdcf-110">Remarks</span></span>

<span data-ttu-id="3fdcf-111">A reprodução é interrompida automaticamente quando um disco é ejetado.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-111">Playback automatically stops when a disc is ejected.</span></span> <span data-ttu-id="3fdcf-112">O aplicativo não precisa executar nenhuma ação especial em resposta a esse evento.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="3fdcf-113">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="3fdcf-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fdcf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fdcf-114">Requirements</span></span>



| <span data-ttu-id="3fdcf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fdcf-115">Requirement</span></span> | <span data-ttu-id="3fdcf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3fdcf-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdcf-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fdcf-117">Header</span></span><br/> | <dl> <span data-ttu-id="3fdcf-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fdcf-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fdcf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fdcf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fdcf-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="3fdcf-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="3fdcf-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="3fdcf-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3fdcf-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3fdcf-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




