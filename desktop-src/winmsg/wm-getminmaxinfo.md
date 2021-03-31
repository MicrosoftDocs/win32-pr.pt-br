---
description: Enviado a uma janela quando o tamanho ou a posição da janela está prestes a ser alterada. Um aplicativo pode usar essa mensagem para substituir o tamanho e a posição padrão da janela, ou seu tamanho de rastreamento mínimo ou máximo padrão.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Mensagem de WM_GETMINMAXINFO (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829209"
---
# <a name="wm_getminmaxinfo-message"></a>Mensagem do WM \_ GETMINMAXINFO

Enviado a uma janela quando o tamanho ou a posição da janela está prestes a ser alterada. Um aplicativo pode usar essa mensagem para substituir o tamanho e a posição padrão da janela, ou seu tamanho de rastreamento mínimo ou máximo padrão.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contém a posição e dimensões maximizadas padrão e os tamanhos de rastreamento mínimo e máximo padrão. Um aplicativo pode substituir os padrões definindo os membros dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

O tamanho máximo de rastreamento é o maior tamanho de janela que pode ser produzido usando as bordas para dimensionar a janela. O tamanho mínimo de rastreamento é o menor tamanho de janela que pode ser produzido usando as bordas para dimensionar a janela.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
