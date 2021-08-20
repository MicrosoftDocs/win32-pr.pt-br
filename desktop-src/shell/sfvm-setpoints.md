---
description: Define os pontos dos objetos atualmente selecionados para o objeto de dados nos comandos copiar e recortar. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_SETPOINTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b994eb7eabe28d20f8f5708dee0cde60be5ae2658d4d83a3691dca3a98a8af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048273"
---
# <a name="sfvm_setpoints-message"></a>Mensagem de SFVM \_ SETpoints

Define os pontos dos objetos atualmente selecionados para o objeto de dados nos comandos **copiar** e **recortar** . Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdtobj* \[ no\]
</dt> <dd>Um ponteiro para um <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> dos comandos **copiar** e **recortar** .</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sempre retorna zero.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
