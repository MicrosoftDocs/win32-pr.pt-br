---
description: Indica que o navegador terminou de reproduzir o segmento especificado em uma chamada para IDvdControl2::P layPeriodInTitleAutoStop.
ms.assetid: 1716eabe-f106-436a-8a6a-ca43cee9341c
title: EC_DVD_PLAYPERIOD_AUTOSTOP (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYPERIOD_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c2081c8a5b7e5b6bd2165781af9552722ed9ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789898"
---
# <a name="ec_dvd_playperiod_autostop"></a><span data-ttu-id="f3eb8-103">autoparada de PLAYPERIOD do EC \_ DVD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f3eb8-103">EC\_DVD\_PLAYPERIOD\_AUTOSTOP</span></span>

<span data-ttu-id="f3eb8-104">Indica que o navegador terminou de reproduzir o segmento especificado em uma chamada para [**IDvdControl2::P layperiodintitleautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span><span class="sxs-lookup"><span data-stu-id="f3eb8-104">Indicates that the Navigator has finished playing the segment specified in a call to [**IDvdControl2::PlayPeriodInTitleAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop).</span></span>

## <a name="parameters"></a><span data-ttu-id="f3eb8-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3eb8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3eb8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f3eb8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f3eb8-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3eb8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f3eb8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f3eb8-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3eb8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3eb8-110">Remarks</span></span>

<span data-ttu-id="f3eb8-111">Esse evento é gerado no domínio do título.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-111">This event is raised in the Title domain.</span></span>

<span data-ttu-id="f3eb8-112">Esse evento também é enviado quando a reprodução é cancelada antes de o navegador concluir a reprodução do segmento especificado.</span><span class="sxs-lookup"><span data-stu-id="f3eb8-112">This event is also sent when playback is canceled before the Navigator finishes playing the specified segment.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eb8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3eb8-113">Requirements</span></span>



| <span data-ttu-id="f3eb8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eb8-114">Requirement</span></span> | <span data-ttu-id="f3eb8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f3eb8-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eb8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3eb8-116">Header</span></span><br/> | <dl> <span data-ttu-id="f3eb8-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3eb8-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3eb8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3eb8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eb8-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="f3eb8-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f3eb8-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="f3eb8-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f3eb8-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3eb8-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="f3eb8-122">**IDvdControl2::P layPeriodInTitleAutoStop**</span><span class="sxs-lookup"><span data-stu-id="f3eb8-122">**IDvdControl2::PlayPeriodInTitleAutoStop**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playperiodintitleautostop)
</dt> </dl>

 

 




