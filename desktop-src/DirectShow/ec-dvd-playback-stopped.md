---
description: Indica que a reprodução de DVD foi interrompida. Esse evento é enviado quando um título ou capítulo é concluído e o navegador de DVD não encontra nenhuma outra instrução de ramificação para reprodução subsequente. O evento não é enviado quando o aplicativo para de reproduzir.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748796"
---
# <a name="ec_dvd_playback_stopped"></a><span data-ttu-id="c765b-105">reprodução de DVD do EC \_ \_ \_ interrompida</span><span class="sxs-lookup"><span data-stu-id="c765b-105">EC\_DVD\_PLAYBACK\_STOPPED</span></span>

<span data-ttu-id="c765b-106">Indica que a reprodução de DVD foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="c765b-106">Indicates that DVD playback has been stopped.</span></span> <span data-ttu-id="c765b-107">Esse evento é enviado quando um título ou capítulo é concluído e o [navegador de DVD](dvd-navigator-filter.md) não encontra nenhuma outra instrução de ramificação para reprodução subsequente.</span><span class="sxs-lookup"><span data-stu-id="c765b-107">This event is sent when a title or chapter completes and the [DVD Navigator](dvd-navigator-filter.md) does not find any other branching instruction for subsequent playback.</span></span> <span data-ttu-id="c765b-108">O evento não é enviado quando o aplicativo para de reproduzir.</span><span class="sxs-lookup"><span data-stu-id="c765b-108">The event is not sent when the application stops playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="c765b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c765b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c765b-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="c765b-110"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c765b-111">Um membro da enumeração do [**DVD \_ PB \_ parou**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , indicando por que a reprodução parou.</span><span class="sxs-lookup"><span data-stu-id="c765b-111">A member of the [**DVD\_PB\_STOPPED**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) enumeration, indicating why playback stopped.</span></span>

</dd> <dt>

<span data-ttu-id="c765b-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="c765b-112"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c765b-113">Zero.</span><span class="sxs-lookup"><span data-stu-id="c765b-113">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c765b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c765b-114">Remarks</span></span>

<span data-ttu-id="c765b-115">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="c765b-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="c765b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c765b-116">Requirements</span></span>



| <span data-ttu-id="c765b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c765b-117">Requirement</span></span> | <span data-ttu-id="c765b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c765b-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c765b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c765b-119">Header</span></span><br/> | <dl> <span data-ttu-id="c765b-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c765b-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c765b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c765b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c765b-122">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="c765b-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="c765b-123">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="c765b-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="c765b-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="c765b-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




