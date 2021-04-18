---
description: Postado na fila de mensagens do thread de instalação quando um temporizador expira. A mensagem é postada pela função GetMessage ou PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Mensagem de WM_TIMER (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171000"
---
# <a name="wm_timer-message"></a>Mensagem de timer do WM \_

Postado na fila de mensagens do thread de instalação quando um temporizador expira. A mensagem é postada pela função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O identificador do temporizador.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Um ponteiro para uma função de retorno de chamada definida pelo aplicativo que foi passada para a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) quando o temporizador foi instalado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Você pode processar a mensagem fornecendo um caso **de \_ temporizador do WM** no procedimento de janela. Caso contrário, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) chamará a função de retorno de chamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) especificada na chamada para a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) usada para instalar o temporizador.

A mensagem de **\_ temporizador do WM** é uma mensagem de baixa prioridade. As funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) postam essa mensagem somente quando nenhuma outra mensagem de prioridade mais alta está na fila de mensagens do thread.

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Temporizadores](timers.md)
</dt> </dl>

 

 
