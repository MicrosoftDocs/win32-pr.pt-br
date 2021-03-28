---
description: Enviado pela implementação do menu de contexto padrão para obter o verbo para a ID de comando fornecida no menu de contexto.
title: Mensagem de DFM_GETVERB (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164307"
---
# <a name="dfm_getverb-message"></a>\_Mensagem GETVERBS DFM

Enviado pela implementação do menu de contexto padrão para obter o verbo para a ID de comando fornecida no menu de contexto.


```C++

                DFM_GETVERB 

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

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto do verbo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído. Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada. Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **DFM \_ GETVERBW** (Unicode) e **DFM \_ getverbs** (ANSI)<br/>                 |



 

 




