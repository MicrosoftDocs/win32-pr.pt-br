---
description: 'Notifica o objeto de retorno de chamada que um menu está sendo removido. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_UNMERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968216"
---
# <a name="sfvm_unmergemenu-message"></a>\_Mensagem SFVM UNMERGEMENU

Notifica o objeto de retorno de chamada que um menu está sendo removido. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hmenuCurrent* \[ no\]
</dt> <dd>

O identificador do menu que está sendo removido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
