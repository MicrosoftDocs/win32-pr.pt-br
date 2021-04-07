---
description: Notifica os aplicativos que o sistema está retomando do modo de suspensão ou hibernação. Esse evento é entregue toda vez que o sistema é retomado e não indica se um usuário está presente.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: Evento de PBT_APMRESUMEAUTOMATIC (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828365"
---
# <a name="pbt_apmresumeautomatic-event"></a><span data-ttu-id="37c1b-104">\_Evento PBT APMRESUMEAUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="37c1b-104">PBT\_APMRESUMEAUTOMATIC event</span></span>

<span data-ttu-id="37c1b-105">Notifica os aplicativos que o sistema está retomando do modo de suspensão ou hibernação.</span><span class="sxs-lookup"><span data-stu-id="37c1b-105">Notifies applications that the system is resuming from sleep or hibernation.</span></span> <span data-ttu-id="37c1b-106">Esse evento é entregue toda vez que o sistema é retomado e não indica se um usuário está presente.</span><span class="sxs-lookup"><span data-stu-id="37c1b-106">This event is delivered every time the system resumes and does not indicate whether a user is present.</span></span>

<span data-ttu-id="37c1b-107">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="37c1b-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="37c1b-108">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="37c1b-108">The *wParam* and *lParam* parameters are set as described following.</span></span>

> [!Note]  
> <span data-ttu-id="37c1b-109">Nos sistemas Windows 10, versão 1507 ou posterior, se o sistema estiver retomando do modo de suspensão somente para entrar imediatamente em hibernação, esse evento não será entregue.</span><span class="sxs-lookup"><span data-stu-id="37c1b-109">In Windows 10, version 1507 systems or later, if the system is resuming from sleep only to immediately enter hibernation, this event is not delivered.</span></span> <span data-ttu-id="37c1b-110">Uma mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) não é enviada nesse caso.</span><span class="sxs-lookup"><span data-stu-id="37c1b-110">A [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message is not sent in this case.</span></span>

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="37c1b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37c1b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c1b-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="37c1b-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="37c1b-113">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="37c1b-113">A handle to window.</span></span>

<span data-ttu-id="37c1b-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="37c1b-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="37c1b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="37c1b-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="37c1b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="37c1b-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="37c1b-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="37c1b-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="37c1b-118">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="37c1b-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="37c1b-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="37c1b-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="37c1b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="37c1b-120">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="37c1b-121">Significado</span><span class="sxs-lookup"><span data-stu-id="37c1b-121">Meaning</span></span>                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="37c1b-122"><dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="37c1b-122"><dt>**PBT\_APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="37c1b-123">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="37c1b-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37c1b-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37c1b-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37c1b-125">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="37c1b-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c1b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37c1b-126">Return value</span></span>

<span data-ttu-id="37c1b-127">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="37c1b-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c1b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="37c1b-128">Remarks</span></span>

<span data-ttu-id="37c1b-129">Se o sistema detectar qualquer atividade do usuário após a difusão PBT \_ APMRESUMEAUTOMATIC, ele transmitirá um evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) para permitir que os aplicativos saibam que podem retomar a interação total com o usuário.</span><span class="sxs-lookup"><span data-stu-id="37c1b-129">If the system detects any user activity after broadcasting PBT\_APMRESUMEAUTOMATIC, it will broadcast a [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) event to let applications know they can resume full interaction with the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="37c1b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37c1b-130">Requirements</span></span>



| <span data-ttu-id="37c1b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c1b-131">Requirement</span></span> | <span data-ttu-id="37c1b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="37c1b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c1b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37c1b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="37c1b-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="37c1b-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37c1b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37c1b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="37c1b-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37c1b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37c1b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37c1b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="37c1b-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37c1b-138"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c1b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="37c1b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c1b-140">Eventos de ativação do sistema</span><span class="sxs-lookup"><span data-stu-id="37c1b-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="37c1b-141">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="37c1b-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="37c1b-142">PBT \_ APMRESUMESUSPEND</span><span class="sxs-lookup"><span data-stu-id="37c1b-142">PBT\_APMRESUMESUSPEND</span></span>](pbt-apmresumesuspend.md)
</dt> <dt>

[<span data-ttu-id="37c1b-143">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="37c1b-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




