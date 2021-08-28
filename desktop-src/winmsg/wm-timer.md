---
description: Postado na fila de mensagens do thread de instalação quando um temporizador expira. A mensagem é postada pela função GetMessage ou PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: WM_TIMER mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710026"
---
# <a name="wm_timer-message"></a>Mensagem TIMER \_ WM

Postado na fila de mensagens do thread de instalação quando um temporizador expira. A mensagem é postada pela [**função GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) [**ou PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea)


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

O identificador do temporizador.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Um ponteiro para uma função de retorno de chamada definida pelo aplicativo que foi passada para a [**função SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) quando o temporizador foi instalado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Você pode processar a mensagem fornecendo um **caso DE \_ TIMER WM** no procedimento de janela. Caso contrário, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) chamará a função de retorno de chamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) especificada na chamada para a [**função SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) usada para instalar o temporizador.

A **mensagem TIMER \_ wm** é uma mensagem de baixa prioridade. As [**funções GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) postam essa mensagem somente quando nenhuma outra mensagem de prioridade mais alta está na fila de mensagens do thread.

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**Settimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**Timerproc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Temporizadores](timers.md)
</dt> </dl>

 

 
