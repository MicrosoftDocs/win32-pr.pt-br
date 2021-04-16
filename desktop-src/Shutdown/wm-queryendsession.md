---
description: A mensagem do WM \_ QUERYENDSESSION é enviada quando o usuário opta por encerrar a sessão ou quando um aplicativo chama uma das funções de desligamento do sistema.
ms.assetid: 7ad73444-f1f6-4b73-8450-0580b146a5a6
title: Mensagem de WM_QUERYENDSESSION (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2e2f82388b229523f371c680d6ccc7c4b1e27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753707"
---
# <a name="wm_queryendsession-message"></a><span data-ttu-id="319b7-103">Mensagem do WM \_ QUERYENDSESSION</span><span class="sxs-lookup"><span data-stu-id="319b7-103">WM\_QUERYENDSESSION message</span></span>

<span data-ttu-id="319b7-104">A mensagem do **WM \_ QUERYENDSESSION** é enviada quando o usuário opta por encerrar a sessão ou quando um aplicativo chama uma das funções de desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="319b7-104">The **WM\_QUERYENDSESSION** message is sent when the user chooses to end the session or when an application calls one of the system shutdown functions.</span></span> <span data-ttu-id="319b7-105">Se qualquer aplicativo retornar zero, a sessão não será encerrada.</span><span class="sxs-lookup"><span data-stu-id="319b7-105">If any application returns zero, the session is not ended.</span></span> <span data-ttu-id="319b7-106">O sistema para de enviar mensagens do **WM \_ QUERYENDSESSION** assim que um aplicativo retorna zero.</span><span class="sxs-lookup"><span data-stu-id="319b7-106">The system stops sending **WM\_QUERYENDSESSION** messages as soon as one application returns zero.</span></span>

<span data-ttu-id="319b7-107">Depois de processar essa mensagem, o sistema envia a mensagem de [**\_ EndSession do WM**](wm-endsession.md) com o parâmetro *wParam* definido para os resultados da mensagem **\_ QUERYENDSESSION do WM** .</span><span class="sxs-lookup"><span data-stu-id="319b7-107">After processing this message, the system sends the [**WM\_ENDSESSION**](wm-endsession.md) message with the *wParam* parameter set to the results of the **WM\_QUERYENDSESSION** message.</span></span>

<span data-ttu-id="319b7-108">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="319b7-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc( 
  HWND hwnd,      // handle to window 
  UINT uMsg,      // message identifier 
  WPARAM wParam,  // not used 
  LPARAM lParam   // logoff option
);
```



## <a name="parameters"></a><span data-ttu-id="319b7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="319b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="319b7-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="319b7-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="319b7-111">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="319b7-111">A handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="319b7-112">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="319b7-112">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="319b7-113">O **identificador \_ QUERYENDSESSION do WM** .</span><span class="sxs-lookup"><span data-stu-id="319b7-113">The **WM\_QUERYENDSESSION** identifier.</span></span>

</dd> <dt>

<span data-ttu-id="319b7-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="319b7-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="319b7-115">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="319b7-115">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="319b7-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="319b7-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="319b7-117">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="319b7-117">This parameter can be one or more of the following values.</span></span> <span data-ttu-id="319b7-118">Se esse parâmetro for 0, o sistema está sendo desligado ou reiniciado (não é possível determinar qual evento está ocorrendo).</span><span class="sxs-lookup"><span data-stu-id="319b7-118">If this parameter is 0, the system is shutting down or restarting (it is not possible to determine which event is occurring).</span></span>



| <span data-ttu-id="319b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="319b7-119">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="319b7-120">Significado</span><span class="sxs-lookup"><span data-stu-id="319b7-120">Meaning</span></span>                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENDSESSION_CLOSEAPP"></span><span id="endsession_closeapp"></span><dl> <span data-ttu-id="319b7-121"><dt>**ENDsession \_ CLOSEAPP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="319b7-121"><dt>**ENDSESSION\_CLOSEAPP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="319b7-122">O aplicativo está usando um arquivo que deve ser substituído, o sistema está sendo atendido ou os recursos do sistema estão esgotados.</span><span class="sxs-lookup"><span data-stu-id="319b7-122">The application is using a file that must be replaced, the system is being serviced, or system resources are exhausted.</span></span> <span data-ttu-id="319b7-123">Para obter mais informações, consulte [diretrizes para aplicativos](../rstmgr/guidelines-for-applications.md).</span><span class="sxs-lookup"><span data-stu-id="319b7-123">For more information, see [Guidelines for Applications](../rstmgr/guidelines-for-applications.md).</span></span><br/> |
| <span id="ENDSESSION_CRITICAL"></span><span id="endsession_critical"></span><dl> <span data-ttu-id="319b7-124"><dt>**ENDsession \_**</dt> <dt>0x40000000</dt> crítico</span><span class="sxs-lookup"><span data-stu-id="319b7-124"><dt>**ENDSESSION\_CRITICAL**</dt> <dt>0x40000000</dt></span></span> </dl> | <span data-ttu-id="319b7-125">O aplicativo é forçado a desligar.</span><span class="sxs-lookup"><span data-stu-id="319b7-125">The application is forced to shut down.</span></span><br/>                                                                                                                                                                              |
| <span id="ENDSESSION_LOGOFF"></span><span id="endsession_logoff"></span><dl> <span data-ttu-id="319b7-126"><dt>**ENDsession \_ LOGOFF**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="319b7-126"><dt>**ENDSESSION\_LOGOFF**</dt> <dt>0x80000000</dt></span></span> </dl>       | <span data-ttu-id="319b7-127">O usuário está fazendo logoff.</span><span class="sxs-lookup"><span data-stu-id="319b7-127">The user is logging off.</span></span> <span data-ttu-id="319b7-128">Para obter mais informações, consulte [fazendo logoff](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="319b7-128">For more information, see [Logging Off](logging-off.md).</span></span><br/>                                                                                                                                   |



 

<span data-ttu-id="319b7-129">Observe que esse parâmetro é uma máscara de bits.</span><span class="sxs-lookup"><span data-stu-id="319b7-129">Note that this parameter is a bit mask.</span></span> <span data-ttu-id="319b7-130">Para testar esse valor, use uma operação bit-wise; Não teste a igualdade.</span><span class="sxs-lookup"><span data-stu-id="319b7-130">To test for this value, use a bit-wise operation; do not test for equality.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="319b7-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="319b7-131">Return value</span></span>

<span data-ttu-id="319b7-132">Os aplicativos devem respeitar as intenções do usuário e retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="319b7-132">Applications should respect the user's intentions and return **TRUE**.</span></span> <span data-ttu-id="319b7-133">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna **true** para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="319b7-133">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE** for this message.</span></span>

<span data-ttu-id="319b7-134">Se o desligamento corromper o sistema ou a mídia que está sendo gravada, o aplicativo poderá retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="319b7-134">If shutting down would corrupt the system or media that is being burned, the application can return **FALSE**.</span></span> <span data-ttu-id="319b7-135">No entanto, é uma boa prática respeitar as ações do usuário.</span><span class="sxs-lookup"><span data-stu-id="319b7-135">However, it is good practice to respect the user's actions.</span></span>

## <a name="remarks"></a><span data-ttu-id="319b7-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="319b7-136">Remarks</span></span>

<span data-ttu-id="319b7-137">Quando um aplicativo retorna **true** para essa mensagem, ele recebe a mensagem de [**\_ EndSession do WM**](wm-endsession.md) , independentemente de como os outros aplicativos respondem à mensagem do **WM \_ QUERYENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="319b7-137">When an application returns **TRUE** for this message, it receives the [**WM\_ENDSESSION**](wm-endsession.md) message, regardless of how the other applications respond to the **WM\_QUERYENDSESSION** message.</span></span> <span data-ttu-id="319b7-138">Cada aplicativo deve retornar **true** ou **false** imediatamente após o recebimento dessa mensagem e adiar todas as operações de limpeza até receber a mensagem de **\_ EndSession do WM** .</span><span class="sxs-lookup"><span data-stu-id="319b7-138">Each application should return **TRUE** or **FALSE** immediately upon receiving this message, and defer any cleanup operations until it receives the **WM\_ENDSESSION** message.</span></span>

<span data-ttu-id="319b7-139">Os aplicativos podem exibir uma interface do usuário solicitando as informações do usuário no desligamento, no entanto, isso não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="319b7-139">Applications can display a user interface prompting the user for information at shutdown, however it is not recommended.</span></span> <span data-ttu-id="319b7-140">Após cinco segundos, o sistema exibe informações sobre os aplicativos que estão impedindo o desligamento e permite que o usuário os encerre.</span><span class="sxs-lookup"><span data-stu-id="319b7-140">After five seconds, the system displays information about the applications that are preventing shutdown and allows the user to terminate them.</span></span> <span data-ttu-id="319b7-141">Por exemplo, o Windows XP exibe uma caixa de diálogo, enquanto o Windows Vista exibe uma tela inteira com informações adicionais sobre os aplicativos que bloqueiam o desligamento.</span><span class="sxs-lookup"><span data-stu-id="319b7-141">For example, Windows XP displays a dialog box, while Windows Vista displays a full screen with additional information about the applications blocking shutdown.</span></span> <span data-ttu-id="319b7-142">Se seu aplicativo precisar bloquear ou adiar o desligamento do sistema, use a função [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .</span><span class="sxs-lookup"><span data-stu-id="319b7-142">If your application must block or postpone system shutdown, use the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span> <span data-ttu-id="319b7-143">Para obter mais informações, consulte [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="319b7-143">For more information, see [Shutdown Changes for Windows Vista](shutdown-changes-for-windows-vista.md).</span></span>

<span data-ttu-id="319b7-144">Os aplicativos de console podem usar a função [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para receber a notificação de desligamento.</span><span class="sxs-lookup"><span data-stu-id="319b7-144">Console applications can use the [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) function to receive shutdown notification.</span></span>

<span data-ttu-id="319b7-145">Os aplicativos de serviço podem usar a função [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para receber notificações de desligamento em uma rotina de manipulador.</span><span class="sxs-lookup"><span data-stu-id="319b7-145">Service applications can use the [**RegisterServiceCtrlHandlerEx**](/windows/win32/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) function to receive shutdown notifications in a handler routine.</span></span>

## <a name="examples"></a><span data-ttu-id="319b7-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="319b7-146">Examples</span></span>

<span data-ttu-id="319b7-147">Para obter um exemplo, consulte [fazendo logoff](logging-off.md).</span><span class="sxs-lookup"><span data-stu-id="319b7-147">For an example, see [Logging Off](logging-off.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="319b7-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="319b7-148">Requirements</span></span>



| <span data-ttu-id="319b7-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="319b7-149">Requirement</span></span> | <span data-ttu-id="319b7-150">Valor</span><span class="sxs-lookup"><span data-stu-id="319b7-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="319b7-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="319b7-151">Minimum supported client</span></span><br/> | <span data-ttu-id="319b7-152">Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]</span><span class="sxs-lookup"><span data-stu-id="319b7-152">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                       |
| <span data-ttu-id="319b7-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="319b7-153">Minimum supported server</span></span><br/> | <span data-ttu-id="319b7-154">Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="319b7-154">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="319b7-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="319b7-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="319b7-156"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="319b7-156"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="319b7-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="319b7-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="319b7-158">Fazendo logoff</span><span class="sxs-lookup"><span data-stu-id="319b7-158">Logging Off</span></span>](logging-off.md)
</dt> <dt>

[<span data-ttu-id="319b7-159">Desligando</span><span class="sxs-lookup"><span data-stu-id="319b7-159">Shutting Down</span></span>](shutting-down.md)
</dt> <dt>

[<span data-ttu-id="319b7-160">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="319b7-160">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="319b7-161">**ExitWindows**</span><span class="sxs-lookup"><span data-stu-id="319b7-161">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)
</dt> <dt>

[<span data-ttu-id="319b7-162">**SetProcessShutdownParameters**</span><span class="sxs-lookup"><span data-stu-id="319b7-162">**SetProcessShutdownParameters**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)
</dt> <dt>

[<span data-ttu-id="319b7-163">**EndSession do WM \_**</span><span class="sxs-lookup"><span data-stu-id="319b7-163">**WM\_ENDSESSION**</span></span>](wm-endsession.md)
</dt> </dl>

 

 
