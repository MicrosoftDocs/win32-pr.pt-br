---
title: Mensagem de WM_ACTIVATE (WinUser. h)
description: Enviado para a janela que está sendo ativada e a janela sendo desativada.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Entrada de mouse e teclado de mensagem WM_ACTIVATE
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085427"
---
# <a name="wm_activate-message"></a>Mensagem de ativação do WM \_

Enviado para a janela que está sendo ativada e a janela sendo desativada. Se as janelas usarem a mesma fila de entrada, a mensagem será enviada de forma síncrona, primeiro para o procedimento de janela da janela de nível superior sendo desativada, em seguida, para o procedimento de janela da janela de nível superior que está sendo ativada. Se as janelas usarem filas de entrada diferentes, a mensagem será enviada de forma assíncrona, de modo que a janela seja ativada imediatamente.


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica se a janela está sendo ativada ou desativada. Esse parâmetro pode usar um dos valores a seguir. A palavra de ordem superior especifica o estado minimizado da janela que está sendo ativada ou desativada. Um valor diferente de zero indica que a janela está minimizada.



| Valor                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <dt>**Wa \_ ATIVO**</dt> <dt>1</dt> </dl>                | Ativado por algum método que não seja um clique do mouse (por exemplo, por uma chamada para a função [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) ou pelo uso da interface do teclado para selecionar a janela).<br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <dt>**Wa \_ CLICKACTIVE**</dt> <dt>2</dt> </dl> | Ativado por um clique do mouse.<br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <dt>**Wa \_ Inativo**</dt> <dt>0</dt> </dl>          | Desativado.<br/>                                                                                                                                                                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para a janela que está sendo ativada ou desativada, dependendo do valor do parâmetro *wParam* . Se a palavra de ordem inferior de *wParam* for **wa \_ inativa**, *lParam* será o identificador para a janela que está sendo ativada. Se a palavra de ordem inferior de *wParam* for **wa \_ Active** ou **wa \_ CLICKACTIVE**, *lParam* será o identificador para a janela que está sendo desativada. Esse identificador pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Se a janela estiver sendo ativada e não for minimizada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) definirá o foco do teclado para a janela. Se a janela for ativada por um clique do mouse, ela também receberá uma mensagem do [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) .

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

[**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[**MOUSEACTIVATE do WM \_**](wm-mouseactivate.md)
</dt> <dt>

[**NCACTIVATE do WM \_**](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

