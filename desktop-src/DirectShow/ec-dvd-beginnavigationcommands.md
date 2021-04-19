---
description: Enviado quando um conjunto de comandos de navegação de DVD está sendo iniciado.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754766"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="a603b-103">\_BeginNavigationCommands de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="a603b-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="a603b-104">Enviado quando um conjunto de comandos de navegação de DVD está sendo iniciado.</span><span class="sxs-lookup"><span data-stu-id="a603b-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="a603b-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a603b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a603b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a603b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a603b-107">Um valor da enumeração [**\_ NavCmdType de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) .</span><span class="sxs-lookup"><span data-stu-id="a603b-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a603b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a603b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a603b-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="a603b-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a603b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a603b-110">Remarks</span></span>

<span data-ttu-id="a603b-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="a603b-111">This event is disabled by default.</span></span> <span data-ttu-id="a603b-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ EnableLoggingEvents** como **true**.</span><span class="sxs-lookup"><span data-stu-id="a603b-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a603b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a603b-113">Requirements</span></span>



| <span data-ttu-id="a603b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a603b-114">Requirement</span></span> | <span data-ttu-id="a603b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a603b-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a603b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a603b-116">Header</span></span><br/> | <dl> <span data-ttu-id="a603b-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a603b-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a603b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a603b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a603b-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="a603b-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a603b-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="a603b-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a603b-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="a603b-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




