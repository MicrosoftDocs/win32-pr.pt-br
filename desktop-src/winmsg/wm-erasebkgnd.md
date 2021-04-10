---
description: Enviado quando o plano de fundo da janela deve ser apagado (por exemplo, quando uma janela é redimensionada). A mensagem é enviada para preparar uma parte invalidada de uma janela para pintura.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Mensagem de WM_ERASEBKGND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170447"
---
# <a name="wm_erasebkgnd-message"></a>Mensagem do WM \_ ERASEBKGND

Enviado quando o plano de fundo da janela deve ser apagado (por exemplo, quando uma janela é redimensionada). A mensagem é enviada para preparar uma parte invalidada de uma janela para pintura.


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o contexto do dispositivo.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar diferente de zero se apagar o plano de fundo; caso contrário, ele deve retornar zero.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) apaga o plano de fundo usando o pincel de plano de fundo de classe especificado pelo membro **HbrBackground** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Se **hbrBackground** for **nulo**, o aplicativo deverá processar a mensagem do **WM \_ ERASEBKGND** e apagar o plano de fundo.

Um aplicativo deve retornar diferente de zero em resposta ao **WM \_ ERASEBKGND** se ele processar a mensagem e apagar o plano de fundo; isso indica que não é necessário apagar mais. Se o aplicativo retornar zero, a janela permanecerá marcada para apagamento. (Normalmente, isso indica que o membro **fErase** da estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) será **true**.)

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Ícones](../menurc/icons.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
