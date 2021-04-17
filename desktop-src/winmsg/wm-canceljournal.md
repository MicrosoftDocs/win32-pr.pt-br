---
description: Postado em um aplicativo quando um usuário cancela as atividades de registro em diário do aplicativo. A mensagem é postada com um identificador de janela nulo.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Mensagem de WM_CANCELJOURNAL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811656"
---
# <a name="wm_canceljournal-message"></a>Mensagem do WM \_ CANCELJOURNAL

Postado em um aplicativo quando um usuário cancela as atividades de registro em diário do aplicativo. A mensagem é postada com um identificador de janela **nulo** .


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

## <a name="return-value"></a>Retornar valor

Tipo: **void**

Essa mensagem não retorna um valor. Ele deve ser processado de dentro do loop principal de um aplicativo ou de um procedimento de gancho [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , não de um procedimento de janela.

## <a name="remarks"></a>Comentários

Os modos de registro e reprodução de diário são modos impostos no sistema que permitem que um aplicativo grave ou reproduza entrada do usuário de forma sequencial. O sistema entra nesses modos quando um aplicativo instala um procedimento de gancho [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) ou [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) . Quando o sistema está em um desses modos de registro em diário, os aplicativos devem assumir a leitura da entrada da fila de entrada. Se qualquer aplicativo parar de ler a entrada enquanto o sistema estiver em um modo de registro no diário, outros aplicativos serão forçados a aguardar.

Para garantir um sistema robusto, que não pode se tornar não responsivo por nenhum aplicativo, o sistema cancela automaticamente todas as atividades do diário quando um usuário pressiona CTRL + ESC ou CTRL + ALT + DEL. Em seguida, o sistema desvincula qualquer procedimento de gancho do diário e posta uma mensagem do **WM \_ CANCELJOURNAL** , com um identificador de janela **nulo** , para o aplicativo que define o gancho do diário.

A mensagem do **WM \_ CANCELJOURNAL** tem um identificador de janela **nulo** , portanto, não pode ser expedida para um procedimento de janela. Há duas maneiras de um aplicativo ver uma mensagem do **WM \_ CANCELJOURNAL** : se o aplicativo estiver em execução em seu próprio loop principal, ele deverá capturar a mensagem entre sua chamada para [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) e sua chamada para [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage). Se o aplicativo não estiver em execução em seu próprio loop principal, ele deverá definir um procedimento de gancho de [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (por meio de uma chamada para [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) especificando o tipo de gancho do **qu \_ GETMESSAGE** ) que observa a mensagem.

Quando um aplicativo vê uma mensagem do **WM \_ CANCELJOURNAL** , ele pode assumir duas coisas: o usuário cancelou intencionalmente o registro de diário ou o modo de reprodução, e o sistema já desvinculou nenhum procedimento de registro de diário ou de conexão de reprodução.

Observe que as combinações de teclas mencionadas acima (CTRL + ESC ou CTRL + ALT + DEL) fazem com que o sistema cancele o registro no diário. Se algum aplicativo for desfeito sem resposta, ele dará ao usuário um meio de recuperação. O código de chave virtual [**VK \_ Cancel**](../inputdev/virtual-key-codes.md) (geralmente implementado como a combinação de teclas Ctrl + Break) é o que um aplicativo que está no modo de registro de diário deve observar como um sinal de que o usuário deseja cancelar a atividade de registro em log. A diferença é que observar **VK \_ Cancel** é um comportamento sugerido para o registro em log de aplicativos, enquanto CTRL + ESC ou Ctrl + Alt + Del fazem com que o sistema cancele o registro em log, independentemente do comportamento de um aplicativo de registro no diário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



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

**Conceitua**
</dt> <dt>

[Ganchos](hooks.md)
</dt> </dl>

 

 
