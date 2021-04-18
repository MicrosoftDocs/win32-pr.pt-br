---
description: Notifica os aplicativos de que o sistema retomou a operação depois de ser suspenso.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: Evento de PBT_APMRESUMESUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756693"
---
# <a name="pbt_apmresumesuspend-event"></a><span data-ttu-id="a33c2-103">\_Evento PBT APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="a33c2-103">PBT\_APMRESUMESUSPEND event</span></span>

<span data-ttu-id="a33c2-104">Notifica os aplicativos de que o sistema retomou a operação depois de ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="a33c2-104">Notifies applications that the system has resumed operation after being suspended.</span></span>

<span data-ttu-id="a33c2-105">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="a33c2-105">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="a33c2-106">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="a33c2-106">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="a33c2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a33c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33c2-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a33c2-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a33c2-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="a33c2-109">A handle to window.</span></span>

<span data-ttu-id="a33c2-110"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="a33c2-110"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="a33c2-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a33c2-111">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="a33c2-112">Significado</span><span class="sxs-lookup"><span data-stu-id="a33c2-112">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="a33c2-113"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="a33c2-113"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="a33c2-114">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a33c2-114">Message identifier.</span></span><br/> |



 

<span data-ttu-id="a33c2-115"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="a33c2-115"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="a33c2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a33c2-116">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="a33c2-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a33c2-117">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="a33c2-118"><dt>**PBT \_ APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="a33c2-118"><dt>**PBT\_APMRESUMESUSPEND**</dt> <dt>7 (0x7)</dt></span></span> </dl> | <span data-ttu-id="a33c2-119">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="a33c2-119">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a33c2-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a33c2-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a33c2-121">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a33c2-121">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33c2-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a33c2-122">Return value</span></span>

<span data-ttu-id="a33c2-123">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a33c2-123">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33c2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="a33c2-124">Remarks</span></span>

<span data-ttu-id="a33c2-125">Um aplicativo poderá receber esse evento somente se ele recebeu o evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de o computador ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="a33c2-125">An application can receive this event only if it received the [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended.</span></span> <span data-ttu-id="a33c2-126">Caso contrário, o aplicativo receberá um evento [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) .</span><span class="sxs-lookup"><span data-stu-id="a33c2-126">Otherwise, the application will receive a [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event.</span></span>

<span data-ttu-id="a33c2-127">Se o sistema for ativado devido à atividade do usuário (como pressionar o botão de energia) ou se o sistema detectar a interação do usuário no console físico (como entrada do mouse ou do teclado) após a ativação autônoma, o sistema primeiro transmite o evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) e, em seguida, transmite o \_ evento PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="a33c2-127">If the system wakes due to user activity (such as pressing the power button) or if the system detects user interaction at the physical console (such as mouse or keyboard input) after waking unattended, the system first broadcasts the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event, then it broadcasts the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="a33c2-128">Além disso, o sistema ativa a exibição.</span><span class="sxs-lookup"><span data-stu-id="a33c2-128">In addition, the system turns on the display.</span></span> <span data-ttu-id="a33c2-129">Seu aplicativo deve reabrir os arquivos que ele fechou quando o sistema entrou em suspensão e se preparar para a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="a33c2-129">Your application should reopen files that it closed when the system entered sleep and prepare for user input.</span></span>

<span data-ttu-id="a33c2-130">Se o sistema for ativado devido a um sinal de ativação externo (ativação remota), o sistema transmitirá apenas o evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .</span><span class="sxs-lookup"><span data-stu-id="a33c2-130">If the system wakes due to an external wake signal (remote wake), the system broadcasts only the [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) event.</span></span> <span data-ttu-id="a33c2-131">O \_ evento PBT APMRESUMESUSPEND não é enviado.</span><span class="sxs-lookup"><span data-stu-id="a33c2-131">The PBT\_APMRESUMESUSPEND event is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33c2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33c2-132">Requirements</span></span>



| <span data-ttu-id="a33c2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33c2-133">Requirement</span></span> | <span data-ttu-id="a33c2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a33c2-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33c2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a33c2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a33c2-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a33c2-136">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a33c2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a33c2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a33c2-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a33c2-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a33c2-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a33c2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33c2-140"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a33c2-140"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33c2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a33c2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33c2-142">Eventos de ativação do sistema</span><span class="sxs-lookup"><span data-stu-id="a33c2-142">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="a33c2-143">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="a33c2-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="a33c2-144">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="a33c2-144">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="a33c2-145">PBT \_ APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="a33c2-145">PBT\_APMRESUMECRITICAL</span></span>](pbt-apmresumecritical.md)
</dt> <dt>

[<span data-ttu-id="a33c2-146">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a33c2-146">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




