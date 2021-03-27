---
description: Enviado pela implementação do menu de contexto padrão para atribuir um nome a um comando de menu.
title: Mensagem de DFM_MAPCOMMANDNAME (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501424"
---
# <a name="dfm_mapcommandname-message"></a>\_Mensagem DFM MAPCOMMANDNAME

Enviado pela implementação do menu de contexto padrão para atribuir um nome a um comando de menu.


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*definição de padrão* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para a ID do comando de menu selecionado.

</dd> <dt>

*pszCommandName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode que contém o nome do comando.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é implementado. Há duas APIs para sua implementação, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada. Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




