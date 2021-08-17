---
title: WM_MENUCOMMAND mensagem (Winuser.h)
description: Enviado quando o usuário faz uma seleção de um menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND menus de mensagem e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d97f629b5d4b0c245606b36efea9ebcb230c4c9fd14d837e18949880a7e7e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971805"
---
# <a name="wm_menucommand-message"></a>Mensagem \_ WM MENUCOMMAND

Enviado quando o usuário faz uma seleção de um menu.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item selecionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para o menu do item selecionado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **mensagem \_ WM MENUCOMMAND** fornece uma alça para o menu para que você possa acessar os dados de menu na estrutura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) e também fornece o índice do item selecionado, que normalmente é o que os aplicativos precisam. Por outro lado, a [**mensagem WM \_ COMMAND**](wm-command.md) fornece o identificador do item de menu.

A **mensagem \_ WM MENUCOMMAND** é enviada somente para menus definidos com o sinalizador **MNS \_ NOTIFYBYPOS** definido no **membro dwStyle** da estrutura [**MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de menus](menus.md)
</dt> </dl>

 

 





