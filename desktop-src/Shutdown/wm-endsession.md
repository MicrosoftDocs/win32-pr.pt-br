---
description: A \_ mensagem de EndSession do WM é enviada para um aplicativo depois que o sistema processa os resultados da mensagem do WM \_ QUERYENDSESSION. A \_ mensagem de EndSession do WM informa ao aplicativo se a sessão está terminando.
ms.assetid: 9bf04f24-da1e-4680-a47b-28e9c500635e
title: Mensagem de WM_ENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa62f356d881182dd6e6fd9e0558332bcc1b3fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755544"
---
# <a name="wm_endsession-message"></a><span data-ttu-id="3f86b-104">\_Mensagem de ENDsession do WM</span><span class="sxs-lookup"><span data-stu-id="3f86b-104">WM\_ENDSESSION message</span></span>

<span data-ttu-id="3f86b-105">A mensagem de **\_ EndSession do WM** é enviada para um aplicativo depois que o sistema processa os resultados da mensagem do [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) .</span><span class="sxs-lookup"><span data-stu-id="3f86b-105">The **WM\_ENDSESSION** message is sent to an application after the system processes the results of the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message.</span></span> <span data-ttu-id="3f86b-106">A mensagem de **\_ EndSession do WM** informa ao aplicativo se a sessão está terminando.</span><span class="sxs-lookup"><span data-stu-id="3f86b-106">The **WM\_ENDSESSION** message informs the application whether the session is ending.</span></span>

<span data-ttu-id="3f86b-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3f86b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // end-session option 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="3f86b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f86b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f86b-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="3f86b-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="3f86b-110">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="3f86b-110">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="3f86b-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="3f86b-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="3f86b-112">O identificador de **\_ EndSession do WM** .</span><span class="sxs-lookup"><span data-stu-id="3f86b-112">The **WM\_ENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3f86b-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f86b-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f86b-114">Se a sessão estiver sendo finalizada, esse parâmetro será **true**; a sessão pode terminar a qualquer momento depois que todos os aplicativos forem retornados do processamento dessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="3f86b-114">If the session is being ended, this parameter is **TRUE**; the session can end any time after all applications have returned from processing this message.</span></span> <span data-ttu-id="3f86b-115">Caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="3f86b-115">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3f86b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f86b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f86b-117">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f86b-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="3f86b-118">Se esse parâmetro for 0, o sistema está sendo desligado ou reiniciado (não é possível determinar qual evento está ocorrendo).</span><span class="sxs-lookup"><span data-stu-id="3f86b-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="3f86b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3f86b-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="3f86b-120">Significado</span><span class="sxs-lookup"><span data-stu-id="3f86b-120">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="3f86b-121"><dt>**ENDsession \_ CLOSEAPP**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="3f86b-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x1</dt></span></span> </dl>        | <span data-ttu-id="3f86b-122">Se *wParam* for **true**, o aplicativo deverá ser desligado.</span><span class="sxs-lookup"><span data-stu-id="3f86b-122">If *wParam* is **TRUE**, the application must shut down.</span></span> <span data-ttu-id="3f86b-123">Todos os dados devem ser salvos automaticamente sem avisar o usuário (para obter mais informações, consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="3f86b-123">Any data should be saved automatically without prompting the user (for more information, see Remarks).</span></span> <span data-ttu-id="3f86b-124">O Gerenciador de reinicialização envia essa mensagem quando o aplicativo está usando um arquivo que precisa ser substituído, quando ele deve atender ao sistema ou quando os recursos do sistema são esgotados.</span><span class="sxs-lookup"><span data-stu-id="3f86b-124">The Restart Manager sends this message when the application is using a file that needs to be replaced, when it must service the system, or when system resources are exhausted.</span></span> <span data-ttu-id="3f86b-125">O aplicativo será reiniciado se tiver sido registrado para reinicialização usando a função [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) .</span><span class="sxs-lookup"><span data-stu-id="3f86b-125">The application will be restarted if it has registered for restart using the [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) function.</span></span> <span data-ttu-id="3f86b-126">Para obter mais informações, consulte [diretrizes para aplicativos](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3f86b-126">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span> <br/> <span data-ttu-id="3f86b-127">Se *wParam* for **false**, o aplicativo não deverá ser desligado.</span><span class="sxs-lookup"><span data-stu-id="3f86b-127">If *wParam* is **FALSE**, the application should not shut down.</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="3f86b-128"><dt>**ENDsession \_**</dt> <dt>0x40000000</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="3f86b-128"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="3f86b-129">O aplicativo é forçado a desligar.</span><span class="sxs-lookup"><span data-stu-id="3f86b-129">The application is forced to shut down.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="3f86b-130"><dt>**ENDsession \_ LOGOFF**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="3f86b-130"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="3f86b-131">O usuário está fazendo logoff.</span><span class="sxs-lookup"><span data-stu-id="3f86b-131">The user is logging off.</span></span> <span data-ttu-id="3f86b-132">Para obter mais informações, consulte [fazendo logoff](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="3f86b-132">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="3f86b-133">Observe que esse parâmetro é uma máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="3f86b-133">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="3f86b-134">Para testar esse valor, use uma operação bit-wise; Não teste a igualdade.</span><span class="sxs-lookup"><span data-stu-id="3f86b-134">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f86b-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f86b-135">Return value</span></span>

<span data-ttu-id="3f86b-136">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="3f86b-136">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f86b-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f86b-137">Remarks</span></span>

<span data-ttu-id="3f86b-138">Os aplicativos que têm dados não salvos podem salvar os dados em um local temporário e restaurá-los na próxima vez que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="3f86b-138">Applications that have unsaved data could save the data to a temporary location and restore it the next time the application starts.</span></span> <span data-ttu-id="3f86b-139">É recomendável que os aplicativos salvem seus dados e Estados com frequência; por exemplo, salve automaticamente os dados entre as operações de salvamento iniciadas pelo usuário para reduzir a quantidade de dados a serem salvos no desligamento.</span><span class="sxs-lookup"><span data-stu-id="3f86b-139">It is recommended that applications save their data and state frequently; for example, automatically save data between save operations initiated by the user to reduce the amount of data to be saved at shutdown.</span></span>

<span data-ttu-id="3f86b-140">O aplicativo não precisa chamar a função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ou [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) quando a sessão está terminando.</span><span class="sxs-lookup"><span data-stu-id="3f86b-140">The application need not call the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) or [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function when the session is ending.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f86b-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f86b-141">Requirements</span></span>



| <span data-ttu-id="3f86b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f86b-142">Requirement</span></span> | <span data-ttu-id="3f86b-143">Valor</span><span class="sxs-lookup"><span data-stu-id="3f86b-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f86b-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f86b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3f86b-145">Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]</span><span class="sxs-lookup"><span data-stu-id="3f86b-145">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="3f86b-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f86b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3f86b-147">Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3f86b-147">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3f86b-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f86b-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f86b-149"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f86b-149"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f86b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f86b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f86b-151">Fazendo logoff</span><span class="sxs-lookup"><span data-stu-id="3f86b-151">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="3f86b-152">Desligando</span><span class="sxs-lookup"><span data-stu-id="3f86b-152">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="3f86b-153">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="3f86b-153">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="3f86b-154">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="3f86b-154">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[<span data-ttu-id="3f86b-155">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="3f86b-155">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="3f86b-156">**QUERYENDSESSION do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3f86b-156">**WM\_QUERYENDSESSION**</span></span>](wm-queryendsession.md)
</dt> </dl>

 

 
