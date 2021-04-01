---
title: Mensagem de WM_NOTIFY (WinUser. h)
description: Enviado por um controle comum para sua janela pai quando um evento ocorreu ou o controle requer algumas informações.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Controles de WM_NOTIFY de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918692"
---
# <a name="wm_notify-message"></a>Mensagem de notificação do WM \_

Enviado por um controle comum para sua janela pai quando um evento ocorreu ou o controle requer algumas informações.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O identificador do controle comum que envia a mensagem. Não há garantia de que esse identificador seja exclusivo. Um aplicativo deve usar o membro **hwndFrom** ou **IdFrom** da estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (passada como o parâmetro *lParam* ) para identificar o controle.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém o código de notificação e informações adicionais. Para algumas mensagens de notificação, esse parâmetro aponta para uma estrutura maior que tem a estrutura **NMHDR** como seu primeiro membro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado, exceto pelas mensagens de notificação que especificam o contrário.

## <a name="remarks"></a>Comentários

O destino da mensagem deve ser o **HWND** do pai do controle. Esse valor pode ser obtido usando [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), conforme mostrado no exemplo a seguir, em que *m \_ controlHwnd* é o **HWND** do próprio controle.


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



Os aplicativos manipulam a mensagem no procedimento de janela da janela pai, conforme mostrado no exemplo a seguir, que manipula a mensagem de notificação enviada pelo controle personalizado no exemplo anterior.


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



Algumas notificações, principalmente as que estiveram na API há muito tempo, são enviadas como mensagens de comando do [**WM \_**](/windows/desktop/menurc/wm-command) . Para obter mais informações, consulte [Control messages](control-messages.md).

Se o manipulador de mensagens estiver em um procedimento de caixa de diálogo, você deverá usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com DWL \_ MSGRESULT para definir um valor de retorno.

Para sistemas Windows Vista e posteriores, a mensagem de **\_ notificação do WM** não pode ser enviada entre processos.

Muitas notificações estão disponíveis nos formatos ANSI e Unicode. A janela que envia a mensagem de **\_ notificação do WM** usa a mensagem do [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) para determinar qual formato deve ser usado. Consulte o **WM \_ NOTIFYFORMAT** para mais discussões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>WinUser. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NOTIFYFORMAT do WM \_**](wm-notifyformat.md)
</dt> </dl>

 

