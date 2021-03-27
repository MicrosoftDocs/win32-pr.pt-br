---
description: Recupera uma matriz de ponteiros para listas de identificadores de item (PIDLs) para todos os objetos selecionados. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_GETSELECTEDOBJECTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837228"
---
# <a name="sfvm_getselectedobjects-message"></a>\_Mensagem SFVM GETSELECTEDOBJECTS

Recupera uma matriz de ponteiros para listas de identificadores de item (PIDLs) para todos os objetos selecionados. Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppidl* \[ fora\]
</dt> <dd>O endereço de uma matriz de PIDLs dos objetos selecionados no momento.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de itens na matriz.

## <a name="remarks"></a>Comentários

Quando terminar, você deve chamar [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) em cada membro da matriz para liberar a memória.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




