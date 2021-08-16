---
description: Postado em um aplicativo quando um usuário cancela as atividades de diário do aplicativo. A mensagem é postada com um alça de janela NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: WM_CANCELJOURNAL mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8672f86393275c46383c6eb27c7eb1884178b86635ea93bf758de16521e6d2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849332"
---
# <a name="wm_canceljournal-message"></a>Mensagem WM \_ CANCELJOURNAL

Postado em um aplicativo quando um usuário cancela as atividades de diário do aplicativo. A mensagem é postada com um alça **de janela NULL.**


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **void**

Essa mensagem não retorna um valor. Ele deve ser processado de dentro do loop principal de um aplicativo ou de um procedimento de gancho [**GetMessage,**](/windows/win32/api/winuser/nf-winuser-getmessage) não de um procedimento de janela.

## <a name="remarks"></a>Comentários

Os modos de registro e reprodução de diário são modos impostos ao sistema que permitem que um aplicativo grave ou reproduza sequencialmente a entrada do usuário. O sistema entra nesses modos quando um aplicativo instala um procedimento de gancho [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) ou [*JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) Quando o sistema está em qualquer um desses modos de diário, os aplicativos devem se revezar lendo a entrada da fila de entrada. Se qualquer aplicativo parar de ler a entrada enquanto o sistema estiver em um modo de diário, outros aplicativos serão forçados a aguardar.

Para garantir um sistema robusto, um que não pode ser feito sem resposta por nenhum aplicativo, o sistema cancela automaticamente todas as atividades de diário quando um usuário pressiona CTRL+ESC ou CTRL+ALT+DEL. Em seguida, o sistema desaloxa todos os procedimentos de gancho de diário e posta uma mensagem **WM \_ CANCELJOURNAL,** com um alça de janela **NULL,** para o aplicativo que definiu o gancho de diário.

A **mensagem WM \_ CANCELJOURNAL** tem um alça de janela **NULL,** portanto, não pode ser enviada para um procedimento de janela. Há duas maneiras para um aplicativo ver uma mensagem **WM \_ CANCELJOURNAL:** se o aplicativo estiver em execução em seu próprio loop principal, ele deverá capturar a mensagem entre sua chamada para [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) e sua chamada para [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage). Se o aplicativo não estiver em execução em seu próprio loop principal, ele deverá definir um procedimento de gancho [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (por meio de uma chamada para [**SetWindowsHookEx especificando**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) o tipo de gancho **\_ GETMESSAGE WH)** que observa a mensagem.

Quando um aplicativo vê uma mensagem **WM \_ CANCELJOURNAL,** ele pode assumir duas coisas: o usuário cancelou intencionalmente o registro de diário ou o modo de reprodução e o sistema já desahookou qualquer registro de diário ou procedimentos de gancho de reprodução.

Observe que as combinações de teclas mencionadas acima (CTRL+ESC ou CTRL+ALT+DEL) causam o cancelamento do registro em diário pelo sistema. Se qualquer aplicativo não responder, ele dará ao usuário um meio de recuperação. O código de chave virtual CANCEL da [**VK \_**](../inputdev/virtual-key-codes.md) (geralmente implementado como a combinação de teclas CTRL+BREAK) é o que um aplicativo que está no modo de registro de diário deve observar como um sinal de que o usuário deseja cancelar a atividade de diário. A diferença é que assistir ao CANCELAMENTO da **VK \_** é um comportamento sugerido para aplicativos de diário, enquanto CTRL+ESC ou CTRL+ALT+DEL fazem com que o sistema cancele o registro em diário, independentemente do comportamento de um aplicativo de diário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Ganchos](hooks.md)
</dt> </dl>

 

 
