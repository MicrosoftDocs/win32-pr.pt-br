---
description: Remove um objeto da exibição do Shell. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_REMOVEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968234"
---
# <a name="sfvm_removeobject-message"></a>\_Mensagem de REmovimentaçãoobject do SFVM

Remove um objeto da exibição do Shell. Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PIDL* \[ no\]
</dt> <dd>PIDL do objeto a ser removido.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item que foi removido se um item correspondente ao PIDL especificado foi encontrado; caso contrário, retornará-1.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




