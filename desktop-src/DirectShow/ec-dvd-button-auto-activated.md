---
description: Sinaliza que um botão de menu do DVD foi ativado automaticamente por instruções no disco. Isso ocorre quando um menu atinge o tempo limite e o disco especificou um botão para ser ativado automaticamente.
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: EC_DVD_BUTTON_AUTO_ACTIVATED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6a30ddcff32140165d5cb6cb648df84b3360a1b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759301"
---
# <a name="ec_dvd_button_auto_activated"></a><span data-ttu-id="2d6fd-103">\_botão de DVD EC \_ \_ \_ ativado automaticamente</span><span class="sxs-lookup"><span data-stu-id="2d6fd-103">EC\_DVD\_BUTTON\_AUTO\_ACTIVATED</span></span>

<span data-ttu-id="2d6fd-104">Sinaliza que um botão de menu do DVD foi ativado automaticamente por instruções no disco. Isso ocorre quando um menu atinge o tempo limite e o disco especificou um botão para ser ativado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2d6fd-104">Signals that a DVD menu button has been automatically activated per instructions on the disc. This occurs when a menu times out and the disc has specified a button to be automatically activated.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d6fd-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d6fd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d6fd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2d6fd-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2d6fd-107">Valor **DWORD** que indica o botão que foi ativado.</span><span class="sxs-lookup"><span data-stu-id="2d6fd-107">**DWORD** value indicating the button that was activated.</span></span>

</dd> <dt>

<span data-ttu-id="2d6fd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2d6fd-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2d6fd-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="2d6fd-109">Zero.</span></span>

</dd> </dl>

<span data-ttu-id="2d6fd-110">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="2d6fd-110">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d6fd-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d6fd-111">Requirements</span></span>



| <span data-ttu-id="2d6fd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d6fd-112">Requirement</span></span> | <span data-ttu-id="2d6fd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2d6fd-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d6fd-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d6fd-114">Header</span></span><br/> | <dl> <span data-ttu-id="2d6fd-115"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d6fd-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d6fd-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d6fd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d6fd-117">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="2d6fd-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2d6fd-118">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="2d6fd-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2d6fd-119">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="2d6fd-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




