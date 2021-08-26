---
title: Mensagem de WM_SETCURSOR (WinUser. h)
description: Enviado a uma janela se o mouse fizer com que o cursor se mova dentro de uma janela e a entrada do mouse não for capturada.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19dccc4fab0d24dd233133e97b3ddcc71f615d9abb27a4684821099b6ad15802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846866"
---
# <a name="wm_setcursor-message"></a>\_Mensagem de SETcursor do WM

Enviado a uma janela se o mouse fizer com que o cursor se mova dentro de uma janela e a entrada do mouse não for capturada.


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela que contém o cursor.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior de *lParam* especifica o resultado do teste de clique para a posição do cursor. Consulte os valores de retorno para [WM_NCHITTEST](../inputdev/wm-nchittest.md) para obter os valores possíveis.

A palavra de ordem superior do *lParam* especifica a mensagem de janela do mouse que disparou esse evento, como [WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Quando a janela entra no modo de menu, esse valor é zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar **true** para interromper o processamento adicional ou **false** para continuar.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) passa a **mensagem \_ SetCursor do WM** para uma janela pai antes do processamento. Se a janela pai retornar **true**, o processamento adicional será interrompido. Passar a mensagem para a janela pai de uma janela fornece o controle de janela pai sobre a configuração do cursor em uma janela filho. A função **DefWindowProc** também usa essa mensagem para definir o cursor para uma seta se ela não estiver na área do cliente ou para o cursor de classe registrado, se estiver na área do cliente. Se a palavra de ordem inferior do parâmetro *lParam* for **HTERROR** e a palavra de ordem superior de *lParam* especificar que um dos botões do mouse será pressionado, **DefWindowProc** chamará a função [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitua**
</dt> <dt>

[Cursores](cursors.md)
</dt> </dl>

 

