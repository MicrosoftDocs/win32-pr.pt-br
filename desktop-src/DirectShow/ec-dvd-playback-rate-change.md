---
description: Sinaliza que uma alteração de taxa na reprodução de DVD foi iniciada.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758435"
---
# <a name="ec_dvd_playback_rate_change"></a><span data-ttu-id="1b5ea-103">\_alteração da \_ taxa de reprodução de DVD do EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="1b5ea-103">EC\_DVD\_PLAYBACK\_RATE\_CHANGE</span></span>

<span data-ttu-id="1b5ea-104">Sinaliza que uma alteração de taxa na reprodução de DVD foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-104">Signals that a rate change in DVD playback has been initiated.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b5ea-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b5ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5ea-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1b5ea-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1b5ea-107">LONG indicando a nova taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-107">LONG indicating the new playback rate.</span></span> <span data-ttu-id="1b5ea-108">O valor é a taxa de reprodução real multiplicada por 10.000, portanto, a taxa de reprodução é igual a 10000,0/ *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-108">The value is the actual playback rate multiplied by 10,000, so the playback rate equals 10000.0 / *lParam1*.</span></span> <span data-ttu-id="1b5ea-109">Valores menores que zero indicam o modo de reprodução reversa e valores maiores que zero indicam o modo de reprodução de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-109">Values less than zero indicate reverse playback mode, and values greater than zero indicate forward playback mode.</span></span>

</dd> <dt>

<span data-ttu-id="1b5ea-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1b5ea-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1b5ea-111">Zero.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b5ea-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b5ea-112">Remarks</span></span>

<span data-ttu-id="1b5ea-113">Esse evento é gerado no domínio do título.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-113">This event is raised in the title domain.</span></span>

<span data-ttu-id="1b5ea-114">A *taxa* de reprodução é o inverso da *velocidade* de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-114">Playback *rate* is the inverse of playback *speed*.</span></span> <span data-ttu-id="1b5ea-115">Por exemplo, se a velocidade de reprodução for 2x, a taxa será 0,5.</span><span class="sxs-lookup"><span data-stu-id="1b5ea-115">For example, if playback speed is 2x, the rate is 0.5.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b5ea-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b5ea-116">Requirements</span></span>



| <span data-ttu-id="1b5ea-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b5ea-117">Requirement</span></span> | <span data-ttu-id="1b5ea-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1b5ea-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5ea-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b5ea-119">Header</span></span><br/> | <dl> <span data-ttu-id="1b5ea-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b5ea-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b5ea-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b5ea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b5ea-122">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="1b5ea-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1b5ea-123">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="1b5ea-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1b5ea-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b5ea-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




