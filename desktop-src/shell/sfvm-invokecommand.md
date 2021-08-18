---
description: Notifica o objeto de retorno de chamada de que um de seus comandos de barra de ferramentas ou menu foi invocado pelo usuário. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b33eba78e0680fe940569c7a7ccfb4a27c61c3ffcb6eead0f2ff6436ec74f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968645"
---
# <a name="sfvm_invokecommand-message"></a>Mensagem INVOKECOMMAND de SFVM \_

Notifica o objeto de retorno de chamada de que um de seus comandos de barra de ferramentas ou menu foi invocado pelo usuário. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd* \[ em\]
</dt> <dd>

A ID do comando da barra de ferramentas ou item de menu selecionado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem serve essencialmente a mesma função que uma mensagem [**WM \_ COMMAND**](../menurc/wm-command.md) em um procedimento de janela convencional. Ele permite que o objeto de retorno de chamada manipular todos os itens que ele adicionou à ferramenta Windows Explorer ou à barra de menus.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
