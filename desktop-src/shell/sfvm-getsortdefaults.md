---
description: 'Permite que o objeto de retorno de chamada especifique um parâmetro de classificação padrão. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETSORTDEFAULTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968233"
---
# <a name="sfvm_getsortdefaults-message"></a>\_Mensagem SFVM GETSORTDEFAULTS

Permite que o objeto de retorno de chamada especifique um parâmetro de classificação padrão. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iDirection* \[ fora\]
</dt> <dd>

A direção de classificação padrão. Defina esse parâmetro como um valor positivo para classificar em ordem crescente. Defina esse parâmetro como zero ou um valor negativo para classificar em ordem decrescente.

</dd> <dt>

*IColumn* \[ fora\]
</dt> <dd>

A coluna usada para a classificação. Isso será passado para o [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) nos menores 16 bits do seu valor de *lParam* .

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> : **SFVM \_ GETSORTDEFAULTS** não é reconhecido pelo objeto de exibição de pasta do sistema.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
