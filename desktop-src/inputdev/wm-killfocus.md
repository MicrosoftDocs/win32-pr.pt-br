---
title: Mensagem de WM_KILLFOCUS (WinUser. h)
description: Enviado a uma janela imediatamente antes de perder o foco do teclado.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Entrada de mouse e teclado de mensagem WM_KILLFOCUS
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644ea7d82a2ae3f316985a882c284d77f3869a75341142d4372b612d66ada1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757450"
---
# <a name="wm_killfocus-message"></a>Mensagem do WM \_ KILLFOCUS

Enviado a uma janela imediatamente antes de perder o foco do teclado.


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela que recebe o foco do teclado. Este parâmetro pode ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Se um aplicativo estiver exibindo um cursor, o cursor deverá ser destruído neste ponto.

Ao processar essa mensagem, não faça nenhuma chamada de função que exiba ou ative uma janela. Isso faz com que o thread gere controle e pode fazer com que o aplicativo pare de responder às mensagens. Para obter mais informações, consulte [deadlocks de mensagem](/windows/desktop/winmsg/about-messages-and-message-queues).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ SETFOCUS**](wm-setfocus.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

