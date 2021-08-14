---
description: Mensagem de DFM_GETHELPTEXT-permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda.
title: Mensagem de DFM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d1035ae82a8caf4c9ada5a859663d0d20286b433a9bf527831c29157d8dd6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860931"
---
# <a name="dfm_gethelptext-message"></a>\_Mensagem DFM GEThelptext

Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda.


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd \_ cchMax* \[\]
</dt> <dd>

A palavra de ordem inferior desse parâmetro contém a ID de comando. A palavra de ordem superior contém o número de caracteres no buffer *pszText* .

</dd> <dt>

*pszText* \[ fora\]
</dt> <dd>

Uma cadeia de caracteres ANSI terminada em nulo que contém o texto de ajuda.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído. Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada. Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DFM \_ GetHelpText** (ANSI)<br/>                                              |



 

 




