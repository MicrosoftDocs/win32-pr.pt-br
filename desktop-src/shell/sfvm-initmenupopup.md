---
description: 'permite que o objeto de retorno de chamada modifique um menu pop-up do Windows Explorer antes de ser exibido. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592308"
---
# <a name="sfvm_initmenupopup-message"></a>\_Mensagem SFVM INITMENUPOPUP

permite que o objeto de retorno de chamada modifique um menu pop-up do Windows Explorer antes de ser exibido. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd \_ nIndex* \[\]
</dt> <dd>

A palavra de ordem inferior desse parâmetro contém o valor da primeira ID de comando reservada para comandos de cliente. A palavra de ordem superior contém o índice do menu.

</dd> <dt>

*HMENU* \[ entrada, saída\]
</dt> <dd>

A alça do menu.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto de exibição da pasta do sistema envia essa mensagem quando um menu é selecionado, mas antes de ser exibido. Processar esta mensagem se, por exemplo, você precisar habilitar ou desabilitar comandos de menu. O menu pop-up pode ser:

-   O menu arquivo, editar ou exibir.
-   Um menu de nível superior definido pelo cliente.
-   Um submenu definido pelo cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
