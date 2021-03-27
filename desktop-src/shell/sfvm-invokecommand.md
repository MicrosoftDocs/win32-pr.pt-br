---
description: 'Notifica o objeto de retorno de chamada de que um de seus comandos de menu ou de barra de ferramentas foi invocado pelo usuário. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Mensagem de SFVM_INVOKECOMMAND (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837227"
---
# <a name="sfvm_invokecommand-message"></a>\_Mensagem SFVM INVOKECOMMAND

Notifica o objeto de retorno de chamada de que um de seus comandos de menu ou de barra de ferramentas foi invocado pelo usuário. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd* \[ em\]
</dt> <dd>

A ID de comando da barra de ferramentas ou do item de menu selecionado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem serve essencialmente a mesma função que uma mensagem de [**\_ comando do WM**](../menurc/wm-command.md) em um procedimento de janela convencional. Ele permite que o objeto de retorno de chamada manipule quaisquer itens que tenham sido adicionados à ferramenta ou à barra de menus do Windows Explorer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
