---
description: Notifica os aplicativos que um evento de gerenciamento de energia ocorreu.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: Mensagem de WM_POWERBROADCAST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505875"
---
# <a name="wm_powerbroadcast-message"></a><span data-ttu-id="ba52a-103">Mensagem do WM \_ POWERBROADCAST</span><span class="sxs-lookup"><span data-stu-id="ba52a-103">WM\_POWERBROADCAST message</span></span>

<span data-ttu-id="ba52a-104">Notifica os aplicativos que um evento de gerenciamento de energia ocorreu.</span><span class="sxs-lookup"><span data-stu-id="ba52a-104">Notifies applications that a power-management event has occurred.</span></span>

<span data-ttu-id="ba52a-105">Uma janela recebe essa mensagem por meio de sua função **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="ba52a-105">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="ba52a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba52a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba52a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ba52a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ba52a-108">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="ba52a-108">A handle to window.</span></span>

<span data-ttu-id="ba52a-109"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="ba52a-109"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="ba52a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ba52a-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="ba52a-111">Significado</span><span class="sxs-lookup"><span data-stu-id="ba52a-111">Meaning</span></span>                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="ba52a-112"><dt>\* \* \* WM \_ POWERBROADCAST \* \*</dt> \* \* <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-112"><dt>\*\*\*\*WM\_POWERBROADCAST\*\*\*\*</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="ba52a-113">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ba52a-113">Message identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ba52a-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba52a-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba52a-115">O evento de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="ba52a-115">The power-management event.</span></span> <span data-ttu-id="ba52a-116">Esse parâmetro pode ser um dos seguintes identificadores de evento.</span><span class="sxs-lookup"><span data-stu-id="ba52a-116">This parameter can be one of the following event identifiers.</span></span>



| <span data-ttu-id="ba52a-117">Evento</span><span class="sxs-lookup"><span data-stu-id="ba52a-117">Event</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="ba52a-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ba52a-118">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="ba52a-119"><dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-119"><dt>**[PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="ba52a-120">O status de energia foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ba52a-120">Power status has changed.</span></span><br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <span data-ttu-id="ba52a-121"><dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-121"><dt>**[PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt></span></span> </dl>        | <span data-ttu-id="ba52a-122">A operação está sendo retomada automaticamente de um estado de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="ba52a-122">Operation is resuming automatically from a low-power state.</span></span> <span data-ttu-id="ba52a-123">Essa mensagem é enviada toda vez que o sistema é retomado.</span><span class="sxs-lookup"><span data-stu-id="ba52a-123">This message is sent every time the system resumes.</span></span><br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <span data-ttu-id="ba52a-124"><dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-124"><dt>**[PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt></span></span> </dl>                  | <span data-ttu-id="ba52a-125">A operação está sendo retomada de um estado de baixa energia.</span><span class="sxs-lookup"><span data-stu-id="ba52a-125">Operation is resuming from a low-power state.</span></span> <span data-ttu-id="ba52a-126">Essa mensagem será enviada após [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) se a retomada for disparada pela entrada do usuário, como pressionar uma tecla.</span><span class="sxs-lookup"><span data-stu-id="ba52a-126">This message is sent after [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) if the resume is triggered by user input, such as pressing a key.</span></span><br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="ba52a-127"><dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-127"><dt>**[PBT\_APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                          | <span data-ttu-id="ba52a-128">O sistema está suspendendo a operação.</span><span class="sxs-lookup"><span data-stu-id="ba52a-128">System is suspending operation.</span></span><br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="ba52a-129"><dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-129"><dt>**[PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt></span></span> </dl>   | <span data-ttu-id="ba52a-130">Um evento de alteração de configuração de energia foi recebido.</span><span class="sxs-lookup"><span data-stu-id="ba52a-130">A power setting change event has been received.</span></span> <br/>                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="ba52a-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba52a-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba52a-132">Os dados específicos do evento.</span><span class="sxs-lookup"><span data-stu-id="ba52a-132">The event-specific data.</span></span> <span data-ttu-id="ba52a-133">Para a maioria dos eventos, esse parâmetro é reservado e não usado.</span><span class="sxs-lookup"><span data-stu-id="ba52a-133">For most events, this parameter is reserved and not used.</span></span>

<span data-ttu-id="ba52a-134">Se o parâmetro *wParam* for [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md), o parâmetro *lParam* será um ponteiro para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="ba52a-134">If the *wParam* parameter is [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md), the *lParam* parameter is a pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba52a-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba52a-135">Return value</span></span>

<span data-ttu-id="ba52a-136">Um aplicativo deve retornar **true** se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ba52a-136">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba52a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba52a-137">Remarks</span></span>

<span data-ttu-id="ba52a-138">O sistema sempre envia uma mensagem [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) sempre que o sistema é retomado.</span><span class="sxs-lookup"><span data-stu-id="ba52a-138">The system always sends a [PBT\_APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) message whenever the system resumes.</span></span> <span data-ttu-id="ba52a-139">Se o sistema for retomado em resposta à entrada do usuário, como pressionar uma tecla, o sistema também enviará uma mensagem **PBT \_ APMRESUMESUSPEND** depois de enviar PBT \_ APMRESUMEAUTOMATIC.</span><span class="sxs-lookup"><span data-stu-id="ba52a-139">If the system resumes in response to user input such as pressing a key, the system also sends a **PBT\_APMRESUMESUSPEND** message after sending PBT\_APMRESUMEAUTOMATIC.</span></span>

<span data-ttu-id="ba52a-140">**WM \_** As mensagens POWERBROADCAST não fazem distinção entre Estados de baixa energia diferentes.</span><span class="sxs-lookup"><span data-stu-id="ba52a-140">**WM\_POWERBROADCAST** messages do not distinguish between different low-power states.</span></span> <span data-ttu-id="ba52a-141">Um aplicativo pode determinar apenas que o sistema está entrando ou foi retomado de um estado de baixa energia; Ele não pode determinar o estado de energia específico.</span><span class="sxs-lookup"><span data-stu-id="ba52a-141">An application can determine only that the system is entering or has resumed from a low-power state; it cannot determine the specific power state.</span></span> <span data-ttu-id="ba52a-142">O sistema registra os detalhes sobre as transições de estado de energia no log de eventos do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="ba52a-142">The system records details about power state transitions in the Windows System event log.</span></span>

<span data-ttu-id="ba52a-143">Para impedir que o sistema faça a transição para um estado de baixa energia no Windows Vista, um aplicativo deve chamar [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) para informar ao sistema que ele está em uso.</span><span class="sxs-lookup"><span data-stu-id="ba52a-143">To prevent the system from transitioning to a low-power state in Windows Vista, an application must call [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) to inform the system that it is in use.</span></span>

<span data-ttu-id="ba52a-144">As seguintes mensagens não têm suporte em nenhum dos sistemas operacionais especificados na seção requisitos:</span><span class="sxs-lookup"><span data-stu-id="ba52a-144">The following messages are not supported on any of the operating systems specified in the Requirements section:</span></span>

- <span data-ttu-id="ba52a-145">PBT_APMQUERYSTANDBY</span><span class="sxs-lookup"><span data-stu-id="ba52a-145">PBT_APMQUERYSTANDBY</span></span>  
- <span data-ttu-id="ba52a-146">PBT_APMQUERYSTANDBYFAILED</span><span class="sxs-lookup"><span data-stu-id="ba52a-146">PBT_APMQUERYSTANDBYFAILED</span></span>  
- <span data-ttu-id="ba52a-147">PBT_APMSTANDBY</span><span class="sxs-lookup"><span data-stu-id="ba52a-147">PBT_APMSTANDBY</span></span>  
- <span data-ttu-id="ba52a-148">PBT_APMRESUMESTANDBY</span><span class="sxs-lookup"><span data-stu-id="ba52a-148">PBT_APMRESUMESTANDBY</span></span>  

## <a name="requirements"></a><span data-ttu-id="ba52a-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba52a-149">Requirements</span></span>



| <span data-ttu-id="ba52a-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba52a-150">Requirement</span></span> | <span data-ttu-id="ba52a-151">Valor</span><span class="sxs-lookup"><span data-stu-id="ba52a-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba52a-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba52a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ba52a-153">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ba52a-153">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba52a-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba52a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ba52a-155">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba52a-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba52a-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba52a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba52a-157"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba52a-157"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba52a-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba52a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba52a-159">\_Mensagens POWERBROADCAST do WM</span><span class="sxs-lookup"><span data-stu-id="ba52a-159">WM\_POWERBROADCAST Messages</span></span>](wm-powerbroadcast-messages.md)
</dt> <dt>

[<span data-ttu-id="ba52a-160">Mensagens de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="ba52a-160">Power Management Messages</span></span>](power-management-messages.md)
</dt> </dl>

 

 




