---
description: 'Permite que o objeto de retorno de chamada forneça uma página a ser adicionada à folha de propriedades de propriedades do objeto selecionado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_ADDPROPERTYPAGES (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989034"
---
# <a name="sfvm_addpropertypages-message"></a>\_Mensagem SFVM ADDPROPERTYPAGES

Permite que o objeto de retorno de chamada forneça uma página a ser adicionada à folha de propriedades de **Propriedades** do objeto selecionado. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ fora\]
</dt> <dd>

O endereço de uma estrutura de [**\_ \_ dados SFVM PROPPAGE**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem serve essencialmente a mesma função que [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Consulte [criando manipuladores de folha de propriedades](propsheet-handlers.md) para mais discussões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
