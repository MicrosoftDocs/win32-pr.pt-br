---
description: Um aplicativo envia a mensagem do WM \_ MDISETMENU para uma janela de cliente MDI (interface de vários documentos) para substituir o menu inteiro de uma janela de quadro MDI, para substituir o menu janela da janela do quadro ou ambos.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Mensagem de WM_MDISETMENU (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fe87682691c5f113034c20c68cefd81ca3a7018bd44eb868c4f18551cacacd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772065"
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

## <a name="return-value"></a>Valor retornado

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
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



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

 

 
