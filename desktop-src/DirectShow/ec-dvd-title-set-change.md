---
description: Enviado quando o conjunto de títulos de vídeo atual (VTS) é alterado.
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c5685cfb909a7fa24c39dff969076269845a663e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783389"
---
# <a name="ec_dvd_title_set_change"></a><span data-ttu-id="63a90-103">\_alteração de \_ definição de título de DVD do EC \_ \_</span><span class="sxs-lookup"><span data-stu-id="63a90-103">EC\_DVD\_TITLE\_SET\_CHANGE</span></span>

<span data-ttu-id="63a90-104">Enviado quando o conjunto de títulos de vídeo atual (VTS) é alterado.</span><span class="sxs-lookup"><span data-stu-id="63a90-104">Sent when current Video Title Set (VTS) changes.</span></span>

## <a name="parameters"></a><span data-ttu-id="63a90-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63a90-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a90-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="63a90-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="63a90-107">O novo número do conjunto de título do vídeo (VTSN).</span><span class="sxs-lookup"><span data-stu-id="63a90-107">The new Video Title Set Number (VTSN).</span></span>

</dd> <dt>

<span data-ttu-id="63a90-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="63a90-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="63a90-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="63a90-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63a90-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="63a90-110">Remarks</span></span>

<span data-ttu-id="63a90-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="63a90-111">This event is disabled by default.</span></span> <span data-ttu-id="63a90-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ NotifyPositionChange** como **true**.</span><span class="sxs-lookup"><span data-stu-id="63a90-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_NotifyPositionChange** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a90-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63a90-113">Requirements</span></span>



| <span data-ttu-id="63a90-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a90-114">Requirement</span></span> | <span data-ttu-id="63a90-115">Valor</span><span class="sxs-lookup"><span data-stu-id="63a90-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a90-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63a90-116">Header</span></span><br/> | <dl> <span data-ttu-id="63a90-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63a90-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a90-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="63a90-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a90-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="63a90-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="63a90-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="63a90-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="63a90-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="63a90-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




