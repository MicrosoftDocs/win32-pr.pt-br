---
title: Mensagem de WM_WTSSESSION_CHANGE (WinUser. h)
description: Notifica os aplicativos sobre as alterações no estado da sessão.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_WTSSESSION_CHANGE Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644317"
---
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="8a621-104">Mensagem de alteração do WM \_ WTSSESSION \_</span><span class="sxs-lookup"><span data-stu-id="8a621-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="8a621-105">Notifica os aplicativos sobre as alterações no estado da sessão.</span><span class="sxs-lookup"><span data-stu-id="8a621-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="8a621-106">A janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8a621-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="8a621-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a621-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a621-108">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a621-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a621-109">Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="8a621-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="8a621-110">*Mensagem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a621-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a621-111">Especifica a mensagem (**WM \_ WTSSESSION \_ Change**).</span><span class="sxs-lookup"><span data-stu-id="8a621-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="8a621-112">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a621-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a621-113">Código de status que descreve o motivo pelo qual a notificação de alteração de estado de sessão foi enviada.</span><span class="sxs-lookup"><span data-stu-id="8a621-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="8a621-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a621-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="8a621-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Conexão do console** (0x1)</span><span class="sxs-lookup"><span data-stu-id="8a621-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-116">A sessão identificada pelo *lParam* foi conectada ao terminal do console ou à sessão do RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="8a621-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="8a621-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Desconexão do console** (0x2)</span><span class="sxs-lookup"><span data-stu-id="8a621-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-118">A sessão identificada pelo *lParam* foi desconectada do terminal do console ou da sessão do RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="8a621-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="8a621-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Conexão remota** (0x3)</span><span class="sxs-lookup"><span data-stu-id="8a621-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-120">A sessão identificada pelo *lParam* foi conectada ao terminal remoto.</span><span class="sxs-lookup"><span data-stu-id="8a621-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="8a621-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Desconexão remota** (0x4)</span><span class="sxs-lookup"><span data-stu-id="8a621-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-122">A sessão identificada pelo *lParam* foi desconectada do terminal remoto.</span><span class="sxs-lookup"><span data-stu-id="8a621-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="8a621-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Logon de sessão** (0x5)</span><span class="sxs-lookup"><span data-stu-id="8a621-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-124">Um usuário fez logon na sessão identificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="8a621-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="8a621-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Logoff de sessão** (0x6)</span><span class="sxs-lookup"><span data-stu-id="8a621-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-126">Um usuário fez logoff da sessão identificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="8a621-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="8a621-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Bloqueio de sessão** (0x7)</span><span class="sxs-lookup"><span data-stu-id="8a621-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-128">A sessão identificada por *lParam* foi bloqueada.</span><span class="sxs-lookup"><span data-stu-id="8a621-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="8a621-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Desbloqueio de sessão** (0x8)</span><span class="sxs-lookup"><span data-stu-id="8a621-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-130">A sessão identificada por *lParam* foi desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="8a621-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="8a621-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Controle remoto de sessão** (0x9)</span><span class="sxs-lookup"><span data-stu-id="8a621-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-132">A sessão identificada por *lParam* alterou seu status controlado remotamente.</span><span class="sxs-lookup"><span data-stu-id="8a621-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="8a621-133">Para determinar o status, chame [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) e verifique a métrica **SM \_ REMOTECONTROL** .</span><span class="sxs-lookup"><span data-stu-id="8a621-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="8a621-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Criação de sessão** (0xA)</span><span class="sxs-lookup"><span data-stu-id="8a621-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-135">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8a621-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="8a621-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Término da sessão** (0xB)</span><span class="sxs-lookup"><span data-stu-id="8a621-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="8a621-137">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8a621-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8a621-138">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a621-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a621-139">O identificador da sessão.</span><span class="sxs-lookup"><span data-stu-id="8a621-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a621-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a621-140">Return value</span></span>

<span data-ttu-id="8a621-141">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8a621-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a621-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a621-142">Remarks</span></span>

<span data-ttu-id="8a621-143">Essa mensagem é enviada somente para aplicativos que se registraram para receber essa mensagem chamando [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span><span class="sxs-lookup"><span data-stu-id="8a621-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="8a621-144">Exemplos de como os aplicativos podem responder a essa mensagem incluem lançar ou adquirir recursos específicos do console, determinar como uma tela deve ser pintada ou disparar efeitos de animação do console.</span><span class="sxs-lookup"><span data-stu-id="8a621-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a621-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a621-145">Requirements</span></span>



| <span data-ttu-id="8a621-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a621-146">Requirement</span></span> | <span data-ttu-id="8a621-147">Valor</span><span class="sxs-lookup"><span data-stu-id="8a621-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a621-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a621-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8a621-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a621-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="8a621-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a621-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8a621-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a621-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="8a621-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a621-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a621-153"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a621-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a621-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8a621-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a621-155">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="8a621-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="8a621-156">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="8a621-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

