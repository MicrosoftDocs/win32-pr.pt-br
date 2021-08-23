---
description: Adiciona um objeto à exibição shell. Usado pela mensagem SHShellFolderView. \_
title: SFVM_ADDOBJECT mensagem (Shlobj.h)
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
ms.openlocfilehash: 441ddac74e1640b2f836686c171d6fc896cbccee2dd6325c31041903ba610b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661056"
---
# <a name="sfvm_addobject-message"></a>Mensagem ADDOBJECT de SFVM \_

Adiciona um objeto à exibição shell. Usado pela [**mensagem SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pidl* \[ Em\]
</dt> <dd>Um ponteiro para o objeto de interesse a ser acrescentado.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a nova ID do item listview do objeto adicionado se o processo foi bem-sucedido; caso contrário, retornará -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




