---
description: Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z foi alterado como resultado de uma chamada para a função SetWindowPos ou outra função de gerenciamento de janela.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Mensagem de WM_WINDOWPOSCHANGED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090275"
---
# <a name="wm_windowposchanged-message"></a>Mensagem do WM \_ WINDOWPOSCHANGED

Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z foi alterado como resultado de uma chamada para a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou outra função de gerenciamento de janela.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que contém informações sobre o novo tamanho e a posição da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia o [**\_ tamanho do WM**](wm-size.md) e as mensagens de [**\_ movimentação do WM**](wm-move.md) para a janela. O **\_ tamanho do WM** e as mensagens de **\_ movimentação do WM** não serão enviadas se um aplicativo manipular a mensagem do **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**. É mais eficiente executar qualquer processamento de alteração de movimentação ou de tamanho durante a mensagem de **\_ WINDOWPOSCHANGED do WM** sem chamar **DefWindowProc**.

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

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**movimentação do WM \_**](wm-move.md)
</dt> <dt>

[**tamanho do WM \_**](wm-size.md)
</dt> <dt>

[**WINDOWPOSCHANGING do WM \_**](wm-windowposchanging.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
