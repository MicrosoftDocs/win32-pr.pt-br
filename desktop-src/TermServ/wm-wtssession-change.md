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
# <a name="wm_wtssession_change-message"></a>Mensagem de alteração do WM \_ WTSSESSION \_

Notifica os aplicativos sobre as alterações no estado da sessão.

A janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Identificador para a janela.

</dd> <dt>

*Mensagem* \[ no\]
</dt> <dd>

Especifica a mensagem (**WM \_ WTSSESSION \_ Change**).

</dd> <dt>

*wParam* \[ no\]
</dt> <dd>

Código de status que descreve o motivo pelo qual a notificação de alteração de estado de sessão foi enviada. Esse parâmetro pode usar um dos valores a seguir.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Conexão do console** (0x1)


</dt> <dd>

A sessão identificada pelo *lParam* foi conectada ao terminal do console ou à sessão do RemoteFX.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Desconexão do console** (0x2)


</dt> <dd>

A sessão identificada pelo *lParam* foi desconectada do terminal do console ou da sessão do RemoteFX.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Conexão remota** (0x3)


</dt> <dd>

A sessão identificada pelo *lParam* foi conectada ao terminal remoto.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Desconexão remota** (0x4)


</dt> <dd>

A sessão identificada pelo *lParam* foi desconectada do terminal remoto.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Logon de sessão** (0x5)


</dt> <dd>

Um usuário fez logon na sessão identificada por *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Logoff de sessão** (0x6)


</dt> <dd>

Um usuário fez logoff da sessão identificada por *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Bloqueio de sessão** (0x7)


</dt> <dd>

A sessão identificada por *lParam* foi bloqueada.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Desbloqueio de sessão** (0x8)


</dt> <dd>

A sessão identificada por *lParam* foi desbloqueada.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Controle remoto de sessão** (0x9)


</dt> <dd>

A sessão identificada por *lParam* alterou seu status controlado remotamente. Para determinar o status, chame [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) e verifique a métrica **SM \_ REMOTECONTROL** .

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Criação de sessão** (0xA)


</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Término da sessão** (0xB)


</dt> <dd>

Reservado para uso futuro.

</dd> </dl> </dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O identificador da sessão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Essa mensagem é enviada somente para aplicativos que se registraram para receber essa mensagem chamando [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).

Exemplos de como os aplicativos podem responder a essa mensagem incluem lançar ou adquirir recursos específicos do console, determinar como uma tela deve ser pintada ou disparar efeitos de animação do console.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                           |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

