---
description: Adiciona um objeto à exibição do Shell. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_ADDOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989035"
---
# <a name="sfvm_addobject-message"></a>\_Mensagem SFVM ADDobject

Adiciona um objeto à exibição do Shell. Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PIDL* \[ no\]
</dt> <dd>Um ponteiro para o objeto de interesse a ser adicionado.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a nova ID de item ListView do objeto adicionado se o processo foi bem-sucedido; caso contrário, retornará-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




