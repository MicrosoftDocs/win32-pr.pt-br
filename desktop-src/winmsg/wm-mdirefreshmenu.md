---
description: Um aplicativo envia a mensagem do WM \_ MDIREFRESHMENU para uma janela de cliente MDI (interface de vários documentos) para atualizar o menu janela da janela do quadro MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Mensagem de WM_MDIREFRESHMENU (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759270"
---
# <a name="wm_mdirefreshmenu-message"></a>Mensagem do WM \_ MDIREFRESHMENU

Um aplicativo envia a mensagem do **WM \_ MDIREFRESHMENU** para uma janela de cliente MDI (interface de vários documentos) para atualizar o menu janela da janela do quadro MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HMENU**

Se a mensagem tiver sucesso, o valor de retorno será o identificador para o menu de janela do quadro.

Se a mensagem falhar, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Depois de enviar essa mensagem, um aplicativo deve chamar a função [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para atualizar a barra de menus.

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

[**MDISETMENU do WM \_**](wm-mdisetmenu.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 
