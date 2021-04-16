---
description: Sinaliza que um disco DVD foi inserido na unidade.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789644"
---
# <a name="ec_dvd_disc_inserted"></a><span data-ttu-id="312ab-103">\_disco de DVD EC \_ \_ inserido</span><span class="sxs-lookup"><span data-stu-id="312ab-103">EC\_DVD\_DISC\_INSERTED</span></span>

<span data-ttu-id="312ab-104">Sinaliza que um disco DVD foi inserido na unidade.</span><span class="sxs-lookup"><span data-stu-id="312ab-104">Signals that a DVD disc was inserted into the drive.</span></span>

## <a name="parameters"></a><span data-ttu-id="312ab-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="312ab-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="312ab-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="312ab-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="312ab-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="312ab-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="312ab-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="312ab-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="312ab-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="312ab-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="312ab-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="312ab-110">Remarks</span></span>

<span data-ttu-id="312ab-111">A reprodução é iniciada automaticamente quando um disco é inserido.</span><span class="sxs-lookup"><span data-stu-id="312ab-111">Playback automatically begins when a disc is inserted.</span></span> <span data-ttu-id="312ab-112">O aplicativo não precisa executar nenhuma ação especial em resposta a esse evento.</span><span class="sxs-lookup"><span data-stu-id="312ab-112">The application does not have to take any special action in response to this event.</span></span>

<span data-ttu-id="312ab-113">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="312ab-113">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="312ab-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="312ab-114">Requirements</span></span>



| <span data-ttu-id="312ab-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="312ab-115">Requirement</span></span> | <span data-ttu-id="312ab-116">Valor</span><span class="sxs-lookup"><span data-stu-id="312ab-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="312ab-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="312ab-117">Header</span></span><br/> | <dl> <span data-ttu-id="312ab-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="312ab-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="312ab-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="312ab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="312ab-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="312ab-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="312ab-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="312ab-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="312ab-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="312ab-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




