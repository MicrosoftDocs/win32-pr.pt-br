---
description: Enviado para verificar a existência de um comando de menu.
title: DFM_VALIDATECMD mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fd647d5cd6e171cc71e0968abb29d80e7aef5900d43fe4bd4b88f5f49bbdc7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721942"
---
# <a name="dfm_validatecmd-message"></a>Mensagem \_ VALIDATECMD do DFM

Enviado para verificar a existência de um comando de menu.


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd* 
</dt> <dd>O deslocamento do identificador do comando de menu.</dd> <dt>

*lParam* 
</dt> <dd>Não usado. Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o comando existir ou S FALSE caso \_ contrário.

## <a name="remarks"></a>Comentários

Essa mensagem é enviada para a função de retorno de chamada ou o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído. Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX é**](dfm-invokecommandex.md) uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada. Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface são necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




