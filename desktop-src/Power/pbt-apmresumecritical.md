---
description: Notifica os aplicativos de que o sistema retomou a operação.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: Evento de PBT_APMRESUMECRITICAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787470"
---
# <a name="pbt_apmresumecritical-event"></a><span data-ttu-id="0b139-103">\_Evento PBT APMRESUMECRITICAL</span><span class="sxs-lookup"><span data-stu-id="0b139-103">PBT\_APMRESUMECRITICAL event</span></span>

<span data-ttu-id="0b139-104">\[PBT \_ APMRESUMECRITICAL está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="0b139-104">\[PBT\_APMRESUMECRITICAL is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0b139-105">O suporte para esse evento foi removido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0b139-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="0b139-106">Em vez disso, use [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) .\]</span><span class="sxs-lookup"><span data-stu-id="0b139-106">Use [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) instead.\]</span></span>

<span data-ttu-id="0b139-107">Notifica os aplicativos de que o sistema retomou a operação.</span><span class="sxs-lookup"><span data-stu-id="0b139-107">Notifies applications that the system has resumed operation.</span></span> <span data-ttu-id="0b139-108">Esse evento pode indicar que alguns ou todos os aplicativos não receberam um evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="0b139-108">This event can indicate that some or all applications did not receive a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event.</span></span> <span data-ttu-id="0b139-109">Por exemplo, esse evento pode ser transmitido após uma suspensão crítica causada por uma bateria com falha.</span><span class="sxs-lookup"><span data-stu-id="0b139-109">For example, this event can be broadcast after a critical suspension caused by a failing battery.</span></span>

<span data-ttu-id="0b139-110">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="0b139-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="0b139-111">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b139-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="0b139-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b139-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b139-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="0b139-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="0b139-114">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="0b139-114">A handle to window.</span></span>

<span data-ttu-id="0b139-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="0b139-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="0b139-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0b139-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="0b139-117">Significado</span><span class="sxs-lookup"><span data-stu-id="0b139-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="0b139-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="0b139-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="0b139-119">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0b139-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="0b139-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="0b139-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="0b139-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0b139-121">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="0b139-122">Significado</span><span class="sxs-lookup"><span data-stu-id="0b139-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <span data-ttu-id="0b139-123"><dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="0b139-123"><dt>**PBT\_APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="0b139-124">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="0b139-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b139-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b139-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b139-126">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0b139-126">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b139-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b139-127">Return value</span></span>

<span data-ttu-id="0b139-128">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0b139-128">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b139-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b139-129">Remarks</span></span>

<span data-ttu-id="0b139-130">Como uma suspensão crítica ocorre sem notificação anterior, os recursos e os dados disponíveis anteriormente poderão não estar presentes quando o aplicativo receber esse evento.</span><span class="sxs-lookup"><span data-stu-id="0b139-130">Because a critical suspension occurs without prior notification, resources and data previously available may not be present when the application receives this event.</span></span> <span data-ttu-id="0b139-131">O aplicativo deve tentar restaurar seu estado da melhor forma que puder.</span><span class="sxs-lookup"><span data-stu-id="0b139-131">The application should attempt to restore its state to the best of its ability.</span></span> <span data-ttu-id="0b139-132">Durante uma suspensão crítica, o sistema mantém o estado dos discos rígidos locais e DRAM, mas pode não manter conexões de rede.</span><span class="sxs-lookup"><span data-stu-id="0b139-132">While in a critical suspension, the system maintains the state of the DRAM and local hard disks, but may not maintain net connections.</span></span> <span data-ttu-id="0b139-133">Um aplicativo pode precisar executar uma ação em relação aos arquivos que estavam abertos na rede antes da suspensão crítica.</span><span class="sxs-lookup"><span data-stu-id="0b139-133">An application may need to take action with respect to files that were open on the network before critical suspension.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b139-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b139-134">Requirements</span></span>



| <span data-ttu-id="0b139-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b139-135">Requirement</span></span> | <span data-ttu-id="0b139-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0b139-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b139-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b139-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0b139-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0b139-138">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b139-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b139-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0b139-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b139-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b139-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0b139-141">End of client support</span></span><br/>    | <span data-ttu-id="0b139-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b139-142">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="0b139-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0b139-143">End of server support</span></span><br/>    | <span data-ttu-id="0b139-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b139-144">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="0b139-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b139-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b139-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b139-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b139-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b139-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b139-148">Eventos de ativação do sistema</span><span class="sxs-lookup"><span data-stu-id="0b139-148">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="0b139-149">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="0b139-149">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="0b139-150">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0b139-150">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




