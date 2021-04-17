---
description: Sinaliza o início de qualquer ainda (PGC, Cell ou VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748613"
---
# <a name="ec_dvd_still_on"></a><span data-ttu-id="df59e-103">o \_ DVD \_ do EC ainda está \_ ativado</span><span class="sxs-lookup"><span data-stu-id="df59e-103">EC\_DVD\_STILL\_ON</span></span>

<span data-ttu-id="df59e-104">Sinaliza o início de qualquer ainda (PGC, Cell ou VOBU).</span><span class="sxs-lookup"><span data-stu-id="df59e-104">Signals the beginning of any still (PGC, Cell, or VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="df59e-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df59e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df59e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="df59e-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="df59e-107">Valor booliano (**bool**) que indica se os botões estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="df59e-107">Boolean (**BOOL**) value indicating whether buttons are available.</span></span> <span data-ttu-id="df59e-108">Zero (0) indica que os botões estão disponíveis para que o método [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) não funcione.</span><span class="sxs-lookup"><span data-stu-id="df59e-108">Zero (0) indicates buttons are available so the [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) method won't work.</span></span> <span data-ttu-id="df59e-109">Um (1) indica que não há botões disponíveis; portanto, **IDvdControl2:: StillOff** funcionará.</span><span class="sxs-lookup"><span data-stu-id="df59e-109">One (1) indicates no buttons are available, so **IDvdControl2::StillOff** will work.</span></span>

</dd> <dt>

<span data-ttu-id="df59e-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="df59e-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="df59e-111">Valor **DWORD** que indica o número de segundos que o ainda durará.</span><span class="sxs-lookup"><span data-stu-id="df59e-111">**DWORD** value indicating the number of seconds the still will last.</span></span> <span data-ttu-id="df59e-112">0xFFFFFFFF indica ainda um infinito, o que significa aguardar até que o usuário pressione um botão ou até que o aplicativo chame [**IDvdControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span><span class="sxs-lookup"><span data-stu-id="df59e-112">0xFFFFFFFF indicates an infinite still, meaning wait until the user presses a button or until the application calls [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df59e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="df59e-113">Remarks</span></span>

<span data-ttu-id="df59e-114">Todas as combinações de botões e ainda são possíveis (botões ativados com ainda em diante, botões ativados com ainda desativado, botão desativado com ainda ativado, botão desativado com ainda desativado).</span><span class="sxs-lookup"><span data-stu-id="df59e-114">All combinations of buttons and still are possible (buttons on with still on, buttons on with still off, button off with still on, button off with still off).</span></span>

<span data-ttu-id="df59e-115">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="df59e-115">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="df59e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df59e-116">Requirements</span></span>



| <span data-ttu-id="df59e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df59e-117">Requirement</span></span> | <span data-ttu-id="df59e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="df59e-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df59e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df59e-119">Header</span></span><br/> | <dl> <span data-ttu-id="df59e-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df59e-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df59e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="df59e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df59e-122">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="df59e-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="df59e-123">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="df59e-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="df59e-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="df59e-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




