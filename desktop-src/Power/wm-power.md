---
description: Notifica os aplicativos que o sistema, normalmente, um computador pessoal alimentado por bateria, está prestes a entrar em um modo suspenso.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: Mensagem de WM_POWER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770135"
---
# <a name="wm_power-message"></a><span data-ttu-id="fee86-103">Mensagem de energia do WM \_</span><span class="sxs-lookup"><span data-stu-id="fee86-103">WM\_POWER message</span></span>

<span data-ttu-id="fee86-104">Notifica os aplicativos que o sistema, normalmente, um computador pessoal alimentado por bateria, está prestes a entrar em um modo suspenso.</span><span class="sxs-lookup"><span data-stu-id="fee86-104">Notifies applications that the system, typically a battery-powered personal computer, is about to enter a suspended mode.</span></span>

> [!Note]  
> <span data-ttu-id="fee86-105">A mensagem de **\_ energia do WM** está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="fee86-105">The **WM\_POWER** message is obsolete.</span></span> <span data-ttu-id="fee86-106">Ele é fornecido apenas para compatibilidade com aplicativos baseados no Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fee86-106">It is provided only for compatibility with 16-bit Windows-based applications.</span></span> <span data-ttu-id="fee86-107">Os aplicativos devem usar a mensagem [**\_ POWERBROADCAST do WM**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="fee86-107">Applications should use the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span>

 

<span data-ttu-id="fee86-108">Uma janela recebe essa mensagem por meio de sua função **WindowProc** .</span><span class="sxs-lookup"><span data-stu-id="fee86-108">A window receives this message through its **WindowProc** function.</span></span>


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a><span data-ttu-id="fee86-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fee86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee86-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="fee86-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fee86-111">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="fee86-111">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="fee86-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="fee86-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="fee86-113">O identificador de mensagem de **\_ energia do WM** .</span><span class="sxs-lookup"><span data-stu-id="fee86-113">The **WM\_POWER** message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="fee86-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fee86-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fee86-115">A notificação de evento de energia.</span><span class="sxs-lookup"><span data-stu-id="fee86-115">The power-event notification.</span></span> <span data-ttu-id="fee86-116">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fee86-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="fee86-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fee86-117">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="fee86-118">Significado</span><span class="sxs-lookup"><span data-stu-id="fee86-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <span data-ttu-id="fee86-119"><dt>**\_CRITICALRESUME PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="fee86-119"><dt>**PWR\_CRITICALRESUME**</dt></span></span> </dl> | <span data-ttu-id="fee86-120">Indica que o sistema está retomando a operação depois de entrar no modo suspenso sem primeiro transmitir uma mensagem de notificação de **\_ SUSPENDREQUEST PWR** para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fee86-120">Indicates that the system is resuming operation after entering suspended mode without first broadcasting a **PWR\_SUSPENDREQUEST** notification message to the application.</span></span> <span data-ttu-id="fee86-121">Um aplicativo deve executar as ações de recuperação necessárias.</span><span class="sxs-lookup"><span data-stu-id="fee86-121">An application should perform any necessary recovery actions.</span></span><br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <span data-ttu-id="fee86-122"><dt>**\_SUSPENDREQUEST PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="fee86-122"><dt>**PWR\_SUSPENDREQUEST**</dt></span></span> </dl> | <span data-ttu-id="fee86-123">Indica que o sistema está prestes a entrar no modo suspenso.</span><span class="sxs-lookup"><span data-stu-id="fee86-123">Indicates that the system is about to enter suspended mode.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <span data-ttu-id="fee86-124"><dt>**\_SUSPENDRESUME PWR**</dt></span><span class="sxs-lookup"><span data-stu-id="fee86-124"><dt>**PWR\_SUSPENDRESUME**</dt></span></span> </dl>    | <span data-ttu-id="fee86-125">Indica que o sistema está retomando a operação depois de ter inserido o modo suspenso normalmente, ou seja, o sistema transmite uma mensagem de notificação de **\_ SUSPENDREQUEST PWR** para o aplicativo antes de o sistema ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="fee86-125">Indicates that the system is resuming operation after having entered suspended mode normally that is, the system broadcast a **PWR\_SUSPENDREQUEST** notification message to the application before the system was suspended.</span></span> <span data-ttu-id="fee86-126">Um aplicativo deve executar as ações de recuperação necessárias.</span><span class="sxs-lookup"><span data-stu-id="fee86-126">An application should perform any necessary recovery actions.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fee86-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fee86-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fee86-128">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="fee86-128">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee86-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fee86-129">Return value</span></span>

<span data-ttu-id="fee86-130">O valor que um aplicativo retorna depende do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="fee86-130">The value an application returns depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="fee86-131">Se *wParam* for **PWR \_ SUSPENDREQUEST**, o valor de retorno será **PWR \_ falha** ao impedir que o sistema entre no estado suspenso; caso contrário, será **PWR \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fee86-131">If *wParam* is **PWR\_SUSPENDREQUEST**, the return value is **PWR\_FAIL** to prevent the system from entering the suspended state; otherwise, it is **PWR\_OK**.</span></span> <span data-ttu-id="fee86-132">Se *wParam* for **PWR \_ SUSPENDRESUME** ou **PWR \_ CRITICALRESUME**, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="fee86-132">If *wParam* is **PWR\_SUSPENDRESUME** or **PWR\_CRITICALRESUME**, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee86-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="fee86-133">Remarks</span></span>

<span data-ttu-id="fee86-134">Essa mensagem é difundida somente para um aplicativo que está sendo executado em um sistema que está em conformidade com a especificação do BIOS (sistema de entrada/saída) básico do APM (gerenciamento avançado de energia).</span><span class="sxs-lookup"><span data-stu-id="fee86-134">This message is broadcast only to an application that is running on a system that conforms to the Advanced Power Management (APM) basic input/output system (BIOS) specification.</span></span> <span data-ttu-id="fee86-135">A mensagem é transmitida pelo driver de gerenciamento de energia para cada janela retornada pela função **EnumWindows** .</span><span class="sxs-lookup"><span data-stu-id="fee86-135">The message is broadcast by the power-management driver to each window returned by the **EnumWindows** function.</span></span>

<span data-ttu-id="fee86-136">O modo suspenso é o estado em que ocorre a maior quantidade de economia de energia, mas todos os dados operacionais e parâmetros são preservados.</span><span class="sxs-lookup"><span data-stu-id="fee86-136">The suspended mode is the state in which the greatest amount of power savings occurs, but all operational data and parameters are preserved.</span></span> <span data-ttu-id="fee86-137">O conteúdo de RAM (memória de acesso aleatório) é preservado, mas muitos dispositivos provavelmente serão desativados.</span><span class="sxs-lookup"><span data-stu-id="fee86-137">Random-access memory (RAM) contents are preserved, but many devices are likely to be turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee86-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fee86-138">Requirements</span></span>



| <span data-ttu-id="fee86-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fee86-139">Requirement</span></span> | <span data-ttu-id="fee86-140">Valor</span><span class="sxs-lookup"><span data-stu-id="fee86-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fee86-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fee86-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fee86-142">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fee86-142">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fee86-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fee86-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fee86-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fee86-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fee86-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fee86-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee86-146"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fee86-146"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee86-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="fee86-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee86-148">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="fee86-148">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




