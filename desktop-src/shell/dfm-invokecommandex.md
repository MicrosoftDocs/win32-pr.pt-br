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
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501425"
---
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="e016a-103">\_Mensagem DFM INVOKECOMMANDEX</span><span class="sxs-lookup"><span data-stu-id="e016a-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="e016a-104">Enviado pela implementação do menu de contexto padrão para solicitar [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) para invocar um comando de menu estendido.</span><span class="sxs-lookup"><span data-stu-id="e016a-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="e016a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e016a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e016a-106">*idCmd* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e016a-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e016a-107">A ID de comando do comando de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="e016a-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="e016a-108">Os sinalizadores a seguir são reconhecidos.</span><span class="sxs-lookup"><span data-stu-id="e016a-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="e016a-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="e016a-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="e016a-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_mover DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="e016a-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**cópia do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="e016a-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**LINK do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="e016a-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**Propriedades do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="e016a-114">Mostrar a interface do usuário de **Propriedades** do item no qual o menu foi invocado.</span><span class="sxs-lookup"><span data-stu-id="e016a-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="e016a-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="e016a-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="e016a-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_colar DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="e016a-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**exibição de DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="e016a-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="e016a-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="e016a-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="e016a-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="e016a-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="e016a-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="e016a-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="e016a-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="e016a-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_renomear DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="e016a-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e016a-123">*PDFMICS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e016a-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e016a-124">Um ponteiro para uma estrutura [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) que contém argumentos adicionais para o comando de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="e016a-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="e016a-125">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e016a-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e016a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e016a-126">Remarks</span></span>

<span data-ttu-id="e016a-127">Após o recebimento dessa mensagem, sua função deverá retornar S \_ false se você quiser que a implementação padrão invoque o manipulador padrão para o comando.</span><span class="sxs-lookup"><span data-stu-id="e016a-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="e016a-128">Retorne \_ os S ok se a mensagem foi tratada.</span><span class="sxs-lookup"><span data-stu-id="e016a-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="e016a-129">Caso contrário, retorne um código de erro HRESULT padrão.</span><span class="sxs-lookup"><span data-stu-id="e016a-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="e016a-130">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o retorno de chamada é implementado.</span><span class="sxs-lookup"><span data-stu-id="e016a-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="e016a-131">Há duas APIs para a construção de retorno de chamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que usa um ponteiro para uma função de retorno de chamada ou [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) que usa um objeto de retorno de chamada que dá suporte a [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="e016a-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="e016a-132">Os itens nos quais o comando está sendo invocado são fornecidos em um objeto de dados passado para a função de retorno de chamada ou para o método [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="e016a-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="e016a-133">Esse objeto de dados é fornecido pela fonte de dados que implementa o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e016a-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="e016a-134">Para extrair os itens do objeto de dados, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="e016a-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="e016a-135">[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) é uma versão mais simples dessa mensagem que não fornece tantas informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e016a-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="e016a-136">Use **DFM \_ INVOKECOMMAND** se as informações adicionais fornecidas pelo **DFM \_ INVOKECOMMANDEX** não forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="e016a-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e016a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e016a-137">Requirements</span></span>



| <span data-ttu-id="e016a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e016a-138">Requirement</span></span> | <span data-ttu-id="e016a-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e016a-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e016a-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e016a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e016a-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e016a-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e016a-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e016a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e016a-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e016a-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e016a-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e016a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e016a-145"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e016a-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
