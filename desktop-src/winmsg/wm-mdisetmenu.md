---
description: Um aplicativo envia a mensagem do WM \_ MDISETMENU para uma janela de cliente MDI (interface de vários documentos) para substituir o menu inteiro de uma janela de quadro MDI, para substituir o menu janela da janela do quadro ou ambos.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Mensagem de WM_MDISETMENU (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793720"
---
# <a name="wm_mdisetmenu-message"></a>Mensagem do WM \_ MDISETMENU

Um aplicativo envia a mensagem do **WM \_ MDISETMENU** para uma janela de cliente MDI (interface de vários documentos) para substituir o menu inteiro de uma janela de quadro MDI, para substituir o menu janela da janela do quadro ou ambos.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o novo menu da janela de quadros. Se esse parâmetro for **nulo**, o menu janela do quadro não será alterado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o novo menu de janela. Se esse parâmetro for **nulo**, o menu janela não será alterado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HMENU**

Se a mensagem tiver sucesso, o valor de retorno será o identificador para o menu da janela do quadro antigo.

Se a mensagem falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Depois de enviar essa mensagem, um aplicativo deve chamar a função [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para atualizar a barra de menus.

Se essa mensagem substituir o menu janela, os itens de menu da janela filho MDI serão removidos do menu da janela anterior e adicionados ao menu nova janela.

Se uma janela filho MDI for maximizada e essa mensagem substituir o menu de janela do quadro MDI, o ícone do menu janela e o ícone restaurar serão removidos do menu da janela do quadro anterior e adicionados ao menu nova janela do quadro.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**MDIREFRESHMENU do WM \_**](wm-mdirefreshmenu.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 
