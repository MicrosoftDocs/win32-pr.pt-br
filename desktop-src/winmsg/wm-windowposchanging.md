---
description: Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z está prestes a ser alterado como resultado de uma chamada para a função SetWindowPos ou outra função de gerenciamento de janela.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Mensagem de WM_WINDOWPOSCHANGING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f10abcb0692374209c2070a465df7c4a5f18672eebf376378d6fb16cbca537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771936"
---
# <a name="wm_windowposchanging-message"></a>Mensagem do WM \_ WINDOWPOSCHANGING

Enviado a uma janela cujo tamanho, posição ou lugar na ordem Z está prestes a ser alterado como resultado de uma chamada para a função [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) ou outra função de gerenciamento de janela.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WINDOWPOSCHANGING            0x0046
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

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Para uma janela com o [**estilo \_ WS Overlapped**](window-styles.md) ou **WS \_ THICKFRAME** , a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia a mensagem [**\_ GETMINMAXINFO do WM**](wm-getminmaxinfo.md) para a janela. Isso é feito para validar o novo tamanho e a posição da janela e para impor os estilos de cliente [cs \_ BYTEALIGNCLIENT](about-window-classes.md) e cs \_ BYTEALIGNWINDOW. Ao não passar a mensagem do **WM \_ WINDOWPOSCHANGING** para a função **DefWindowProc** , um aplicativo pode substituir esses padrões.

Enquanto essa mensagem está sendo processada, modificar qualquer um dos valores em [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) afeta o novo tamanho, a posição ou o local da janela na ordem Z. Um aplicativo pode impedir alterações na janela definindo ou limpando os bits apropriados no membro **flags** de **WINDOWPOS**.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[**GETMINMAXINFO do WM \_**](wm-getminmaxinfo.md)
</dt> <dt>

[**movimentação do WM \_**](wm-move.md)
</dt> <dt>

[**tamanho do WM \_**](wm-size.md)
</dt> <dt>

[**WINDOWPOSCHANGED do WM \_**](wm-windowposchanged.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
