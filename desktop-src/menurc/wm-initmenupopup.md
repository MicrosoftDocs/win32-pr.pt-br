---
title: Mensagem de WM_INITMENUPOPUP (WinUser. h)
description: WM_INITMENUPOPUP mensagem enviada quando um menu suspenso ou submenu está prestes a ficar ativo. Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba23607dcb8da7fb282e380e87fe6a2cbb9a26a50850845a5877d036983665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869595"
---
# <a name="wm_initmenupopup-message"></a>Mensagem do WM \_ INITMENUPOPUP

Enviado quando um menu suspenso ou submenu está prestes a ficar ativo. Isso permite que um aplicativo modifique o menu antes que ele seja exibido, sem alterar o menu inteiro.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o menu suspenso ou submenu.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a posição relativa de base zero do item de menu que abre o menu suspenso ou o submenu.

A palavra de ordem superior indica se o menu suspenso é o menu janela. Se o menu for o menu janela, esse parâmetro será **true**; caso contrário, será **false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

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

[**INITMENU do WM \_**](wm-initmenu.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

