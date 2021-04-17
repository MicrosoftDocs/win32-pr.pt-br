---
description: Indica que o navegador de DVD começou a reproduzir ou terminou de reproduzir dados do karaokê.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fb83bc1de9c2933b53935c056b192eca74c4245c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783391"
---
# <a name="ec_dvd_karaoke_mode"></a><span data-ttu-id="c14a1-103">\_modo de \_ karaokê de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="c14a1-103">EC\_DVD\_KARAOKE\_MODE</span></span>

<span data-ttu-id="c14a1-104">Indica que o [navegador de DVD](data-flow-in-the-dvd-navigator.md) começou a reproduzir ou terminou de reproduzir dados do karaokê.</span><span class="sxs-lookup"><span data-stu-id="c14a1-104">Indicates that the [DVD Navigator](data-flow-in-the-dvd-navigator.md) has either begun playing or finished playing karaoke data.</span></span>

## <a name="parameters"></a><span data-ttu-id="c14a1-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c14a1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c14a1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c14a1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c14a1-107">$True.</span><span class="sxs-lookup"><span data-stu-id="c14a1-107">Boolean value.</span></span> <span data-ttu-id="c14a1-108">Se for **true**, uma faixa do karaokê será reproduzida.</span><span class="sxs-lookup"><span data-stu-id="c14a1-108">If **TRUE**, a karaoke track is being played.</span></span> <span data-ttu-id="c14a1-109">Caso contrário, nenhuma faixa do karaokê será reproduzida.</span><span class="sxs-lookup"><span data-stu-id="c14a1-109">Otherwise, no karaoke track is being played.</span></span>

</dd> <dt>

<span data-ttu-id="c14a1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c14a1-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c14a1-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c14a1-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c14a1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c14a1-112">Remarks</span></span>

<span data-ttu-id="c14a1-113">O DVD Player sinaliza esse evento sempre que ele altera domínios.</span><span class="sxs-lookup"><span data-stu-id="c14a1-113">The DVD player signals this event whenever it changes domains.</span></span>

<span data-ttu-id="c14a1-114">Esse evento é gerado em todos os domínios de DVD.</span><span class="sxs-lookup"><span data-stu-id="c14a1-114">This event is raised in all DVD domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="c14a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c14a1-115">Requirements</span></span>



| <span data-ttu-id="c14a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c14a1-116">Requirement</span></span> | <span data-ttu-id="c14a1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c14a1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c14a1-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c14a1-118">Header</span></span><br/> | <dl> <span data-ttu-id="c14a1-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c14a1-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c14a1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c14a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14a1-121">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="c14a1-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c14a1-122">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="c14a1-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c14a1-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="c14a1-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




