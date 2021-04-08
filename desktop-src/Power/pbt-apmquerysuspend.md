---
description: Solicita permissão para suspender o computador. Um aplicativo que concede permissão deve realizar preparações para a suspensão antes de retornar.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: Evento de PBT_APMQUERYSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828366"
---
# <a name="pbt_apmquerysuspend-event"></a><span data-ttu-id="24a18-104">\_Evento PBT APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="24a18-104">PBT\_APMQUERYSUSPEND event</span></span>

<span data-ttu-id="24a18-105">\[PBT \_ APMQUERYSUSPEND está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="24a18-105">\[PBT\_APMQUERYSUSPEND is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="24a18-106">O suporte para esse evento foi removido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="24a18-106">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="24a18-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="24a18-107">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="24a18-108">Solicita permissão para suspender o computador.</span><span class="sxs-lookup"><span data-stu-id="24a18-108">Requests permission to suspend the computer.</span></span> <span data-ttu-id="24a18-109">Um aplicativo que concede permissão deve realizar preparações para a suspensão antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="24a18-109">An application that grants permission should carry out preparations for the suspension before returning.</span></span>

<span data-ttu-id="24a18-110">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="24a18-110">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="24a18-111">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="24a18-111">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a><span data-ttu-id="24a18-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24a18-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a18-113">*HWND*</span><span class="sxs-lookup"><span data-stu-id="24a18-113">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="24a18-114">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="24a18-114">A handle to window.</span></span>

<span data-ttu-id="24a18-115"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="24a18-115"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="24a18-116">Valor</span><span class="sxs-lookup"><span data-stu-id="24a18-116">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="24a18-117">Significado</span><span class="sxs-lookup"><span data-stu-id="24a18-117">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="24a18-118"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="24a18-118"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="24a18-119">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="24a18-119">Message identifier.</span></span><br/> |



 

<span data-ttu-id="24a18-120"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="24a18-120"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="24a18-121">Valor</span><span class="sxs-lookup"><span data-stu-id="24a18-121">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="24a18-122">Significado</span><span class="sxs-lookup"><span data-stu-id="24a18-122">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <span data-ttu-id="24a18-123"><dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="24a18-123"><dt>**PBT\_APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="24a18-124">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="24a18-124">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="24a18-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24a18-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24a18-126">Os sinalizadores de ação.</span><span class="sxs-lookup"><span data-stu-id="24a18-126">The action flags.</span></span> <span data-ttu-id="24a18-127">Se o bit 0 for 1, o aplicativo poderá solicitar instruções ao usuário sobre como se preparar para a suspensão; caso contrário, o aplicativo deve se preparar sem interação com o usuário.</span><span class="sxs-lookup"><span data-stu-id="24a18-127">If bit 0 is 1, the application can prompt the user for directions on how to prepare for the suspension; otherwise, the application must prepare without user interaction.</span></span> <span data-ttu-id="24a18-128">Todos os outros valores de bit são reservados.</span><span class="sxs-lookup"><span data-stu-id="24a18-128">All other bit values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a18-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24a18-129">Return value</span></span>

<span data-ttu-id="24a18-130">Retornar **true** para conceder a solicitação para suspender.</span><span class="sxs-lookup"><span data-stu-id="24a18-130">Return **TRUE** to grant the request to suspend.</span></span> <span data-ttu-id="24a18-131">Para negar a solicitação, retorne a **consulta de difusão \_ \_ negar**.</span><span class="sxs-lookup"><span data-stu-id="24a18-131">To deny the request, return **BROADCAST\_QUERY\_DENY**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a18-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="24a18-132">Remarks</span></span>

<span data-ttu-id="24a18-133">Um aplicativo deve processar esse evento o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="24a18-133">An application should process this event as quickly as possible.</span></span> <span data-ttu-id="24a18-134">O aplicativo pode solicitar instruções ao usuário sobre como se preparar para a suspensão somente se o bit 0 no parâmetro *flags* estiver definido.</span><span class="sxs-lookup"><span data-stu-id="24a18-134">The application can prompt the user for directions on how to prepare for suspension only if bit 0 in the *Flags* parameter is set.</span></span> <span data-ttu-id="24a18-135">No entanto, se essa mensagem for emitida porque o usuário está fechando a tampa do laptop, não será possível solicitar o usuário.</span><span class="sxs-lookup"><span data-stu-id="24a18-135">However, if this message is issued because the user is closing the laptop lid, it will not be possible to prompt the user.</span></span> <span data-ttu-id="24a18-136">Os aplicativos devem respeitar que o usuário espera um determinado comportamento quando fecham a tampa do laptop ou pressionam o botão de energia e permitem que a transição tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="24a18-136">Applications should respect that the user expects a certain behavior when they close the laptop lid or press the power button and allow the transition to succeed.</span></span>

<span data-ttu-id="24a18-137">O sistema permite que aproximadamente 20 segundos para um aplicativo remova a mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) que está enviando o \_ evento PBT APMQUERYSUSPEND da fila de mensagens do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24a18-137">The system allows approximately 20 seconds for an application to remove the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message that is sending the PBT\_APMQUERYSUSPEND event from the application's message queue.</span></span> <span data-ttu-id="24a18-138">Se um aplicativo não remover a mensagem de sua fila em menos de 20 segundos, o sistema irá pressupor que o aplicativo está em um estado não responsivo e que o aplicativo concorda com a solicitação de suspensão.</span><span class="sxs-lookup"><span data-stu-id="24a18-138">If an application does not remove the message from its queue in less than 20 seconds, the system will assume that the application is in a non-responsive state, and that the application agrees to the sleep request.</span></span> <span data-ttu-id="24a18-139">Os aplicativos que não processam suas filas de mensagens podem ter suas operações interrompidas.</span><span class="sxs-lookup"><span data-stu-id="24a18-139">Applications that do not process their message queues may have their operations interrupted.</span></span> <span data-ttu-id="24a18-140">Depois de remover a mensagem da fila de mensagens, um aplicativo pode levar tanto tempo quanto necessário para executar as operações necessárias antes de entrar no estado de suspensão.</span><span class="sxs-lookup"><span data-stu-id="24a18-140">After it removes the message from the message queue, an application can take as much time as needed to perform any required operations before entering the sleep state.</span></span> <span data-ttu-id="24a18-141">Qualquer operação que possa demorar mais do que 20 segundos deve ser executada no momento, uma vez que o sistema permite que apenas 20 segundos para que as operações sejam concluídas durante o processamento do [PBT \_ APMSUSPEND](pbt-apmsuspend.md) .</span><span class="sxs-lookup"><span data-stu-id="24a18-141">Any operations that could take longer then 20 seconds should be performed at this time, since the system allows only 20 seconds for operations to complete during [PBT\_APMSUSPEND](pbt-apmsuspend.md) processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a18-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24a18-142">Requirements</span></span>



| <span data-ttu-id="24a18-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a18-143">Requirement</span></span> | <span data-ttu-id="24a18-144">Valor</span><span class="sxs-lookup"><span data-stu-id="24a18-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a18-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24a18-145">Minimum supported client</span></span><br/> | <span data-ttu-id="24a18-146">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="24a18-146">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="24a18-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24a18-147">Minimum supported server</span></span><br/> | <span data-ttu-id="24a18-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24a18-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24a18-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="24a18-149">End of client support</span></span><br/>    | <span data-ttu-id="24a18-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="24a18-150">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="24a18-151">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="24a18-151">End of server support</span></span><br/>    | <span data-ttu-id="24a18-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="24a18-152">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="24a18-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24a18-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="24a18-154"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24a18-154"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a18-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="24a18-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a18-156">Eventos de ativação do sistema</span><span class="sxs-lookup"><span data-stu-id="24a18-156">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="24a18-157">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="24a18-157">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="24a18-158">PBT \_ APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="24a18-158">PBT\_APMSUSPEND</span></span>](pbt-apmsuspend.md)
</dt> <dt>

[<span data-ttu-id="24a18-159">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="24a18-159">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




