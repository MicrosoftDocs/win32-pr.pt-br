---
description: Notifica o objeto de retorno de chamada de que a janela de exibição de pasta está sendo criada. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_WINDOWCREATED mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2d09957e1164d5caacbddc23c9a72cb33ef80ffa156dd0538c0be1e24f192018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111156"
---
# <a name="sfvm_windowcreated-message"></a>Mensagem SFVM \_ WINDOWCREATED

Notifica o objeto de retorno de chamada de que a janela de exibição de pasta está sendo criada. Usado por [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndView* \[ Em\]
</dt> <dd>

O alça de janela da exibição de pasta.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
