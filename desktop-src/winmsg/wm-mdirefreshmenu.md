---
description: Um aplicativo envia a mensagem WM MDIREFRESHMENU para uma janela de cliente MDI (interface MDI) para atualizar o menu de janela da janela de quadro \_ MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: WM_MDIREFRESHMENU mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 707059d3cc51703819968f929f9692dbb2422ee3f9fa77e2edb697f12257faf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200062"
---
# <a name="wm_mdirefreshmenu-message"></a>Mensagem WM \_ MDIREFRESHMENU

Um aplicativo envia a **mensagem WM \_ MDIREFRESHMENU** para uma janela de cliente MDI (interface MDI) para atualizar o menu de janela da janela de quadro MDI.


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

## <a name="return-value"></a>Valor retornado

Tipo: **HMENU**

Se a mensagem for bem-sucedida, o valor de retorno será o alçamento para o menu da janela do quadro.

Se a mensagem falhar, o valor de retorno será **NULL.**

## <a name="remarks"></a>Comentários

Depois de enviar essa mensagem, um aplicativo deve chamar a [**função DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para atualizar a barra de menus.

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

[**Drawmenubar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ MDISETMENU**](wm-mdisetmenu.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Interface de vários documentos](multiple-document-interface.md)
</dt> </dl>

 

 
