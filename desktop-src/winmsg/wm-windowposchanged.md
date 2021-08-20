---
description: Enviado para uma janela cujo tamanho, posição ou local na ordem Z foi alterado como resultado de uma chamada para a função SetWindowPos ou outra função de gerenciamento de janela.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: WM_WINDOWPOSCHANGED mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e0900ba4f48b100bad9faf8112df974dee9ba8bfe89c95422698f94cf165c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030815"
---
# <a name="wm_windowposchanged-message"></a>Mensagem WM \_ WINDOWPOSCHANGED

Enviado para uma janela cujo tamanho, posição ou local na ordem Z foi alterado como resultado de uma chamada para a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou outra função de gerenciamento de janela.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Um ponteiro para uma [**estrutura WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que contém informações sobre o novo tamanho e a posição da janela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Por padrão, a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia as [**mensagens WM \_ SIZE**](wm-size.md) e [**WM \_ MOVE**](wm-move.md) para a janela. As **mensagens WM \_ SIZE** e **WM \_ MOVE** não serão enviadas se um aplicativo manipular a mensagem **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**. É mais eficiente executar qualquer movimentação ou processamento de alteração de tamanho durante a mensagem **WM \_ WINDOWPOSCHANGED** sem chamar **DefWindowProc**.

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

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Enddeferwindowpos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**Setwindowpos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**TAMANHO \_ DO WM**](wm-size.md)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
