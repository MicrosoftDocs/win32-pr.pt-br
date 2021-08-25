---
description: Enviado pela implementação do menu de contexto padrão para solicitar LPFNDFMCALLBACK para invocar um comando de menu estendido.
title: Mensagem de DFM_INVOKECOMMANDEX (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2b8a7fd63aa4269ee265a4ae147c99fe394e8aad725f7134f8d62daf8ee9984b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943166"
---
# <a name="dfm_invokecommandex-message"></a>\_Mensagem DFM INVOKECOMMANDEX

Enviado pela implementação do menu de contexto padrão para solicitar [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) para invocar um comando de menu estendido.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*idCmd* \[ em\]
</dt> <dd>

A ID de comando do comando de menu selecionado. Os sinalizadores a seguir são reconhecidos.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_mover DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**cópia do DFM \_ cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**LINK do DFM \_ cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**Propriedades do DFM \_ cmd \_**


</dt> <dd>

Mostrar a interface do usuário de **Propriedades** do item no qual o menu foi invocado.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_colar DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**exibição de DFM \_ cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_renomear DFM cmd \_**


</dt> <dd></dd> </dl> </dd> <dt>

*PDFMICS* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) que contém argumentos adicionais para o comando de menu selecionado. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Após o recebimento dessa mensagem, sua função deverá retornar S \_ false se você quiser que a implementação padrão invoque o manipulador padrão para o comando. Retorne \_ os S ok se a mensagem foi tratada. Caso contrário, retorne um código de erro HRESULT padrão.

Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o retorno de chamada é implementado. Há duas APIs para a construção de retorno de chamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que usa um ponteiro para uma função de retorno de chamada ou [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) que usa um objeto de retorno de chamada que dá suporte a [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).

Os itens nos quais o comando está sendo invocado são fornecidos em um objeto de dados passado para a função de retorno de chamada ou para o método [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) . Esse objeto de dados é fornecido pela fonte de dados que implementa o retorno de chamada. Para extrair os itens do objeto de dados, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) é uma versão mais simples dessa mensagem que não fornece tantas informações para o retorno de chamada. Use **DFM \_ INVOKECOMMAND** se as informações adicionais fornecidas pelo **DFM \_ INVOKECOMMANDEX** não forem necessárias em sua implementação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
