---
description: Enviado pela implementação do menu de contexto padrão durante a criação, especificando o comando de menu padrão e permitindo que uma escolha alternativa seja feita. Usado por LPFNDFMCALLBACK.
title: Mensagem de DFM_GETDEFSTATICID (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370611"
---
# <a name="dfm_getdefstaticid-message"></a>\_Mensagem DFM GETDEFSTATICID

Enviado pela implementação do menu de contexto padrão durante a criação, especificando o comando de menu padrão e permitindo que uma escolha alternativa seja feita. Usado por [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*definição de padrão* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para a ID do comando de menu selecionado. O sinalizador a seguir é reconhecido.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**Propriedades do DFM \_ cmd \_**


</dt> <dd>

Mostrar a interface do usuário de **Propriedades** do item no qual o menu foi invocado.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Para substituir a opção de comando padrão, seu manipulador deve, após o recebimento dessa mensagem, definir o valor apontado por *DefaultID* para a ID do comando de substituição e retornar S \_ OK. Caso contrário, retorna um código de falha.

Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído. Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada. Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
