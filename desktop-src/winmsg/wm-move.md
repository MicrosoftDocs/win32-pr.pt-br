---
description: Enviado após uma janela ser movida.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Mensagem de WM_MOVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84c18d7a4f4411f45a3338a057a60942d01905ccefd25b40ee511d3b8a5d915d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810466"
---
# <a name="wm_move-message"></a>Mensagem de movimentação do WM \_

Enviado após uma janela ser movida.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

As coordenadas x e y do canto superior esquerdo da área do cliente da janela. A palavra de ordem inferior contém a coordenada x, enquanto a palavra de ordem superior contém a coordenada y.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Os parâmetros são fornecidos em coordenadas de tela para janelas sobrepostas e pop-up e em coordenadas de cliente pai para janelas filhas.

O exemplo a seguir demonstra como obter a posição do parâmetro *lParam* .


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



Você também pode usar a macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) para converter o parâmetro *lParam* em uma estrutura [**Points**](/previous-versions//dd162808(v=vs.85)) .

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia o **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** quando processa a mensagem do [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .
O **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** não serão enviadas se um aplicativo manipular a mensagem do **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WINDOWPOSCHANGED do WM \_**](wm-windowposchanged.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**FAIXAS**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
