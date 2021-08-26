---
description: Permite que o retorno de chamada adicione itens à parte inferior do menu estendido.
title: Mensagem de DFM_MERGECONTEXTMENU_BOTTOM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 11dade0f4b9526fa3c384f612b2c23eb77b437ef361d16c2adffc0a49df2ca28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111836"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>Mensagem de DFM \_ MERGECONTEXTMENU \_ inferior

Permite que o retorno de chamada adicione itens à parte inferior do menu estendido.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pqcminfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contém as informações usadas na mesclagem.

</dd> <dt>

*uFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam como o menu de contexto pode ser alterado. Esse parâmetro usa os valores de CMF \_ \* descritos em [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Comentários

Se os itens forem adicionados ao menu de contexto estendido, eles deverão ter suporte com rotinas que respondem adequadamente quando um desses itens é invocado usando [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).

Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído. Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada. Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




