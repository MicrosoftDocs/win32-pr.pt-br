---
description: Enviado pela implementação do menu de contexto padrão para solicitar a função de retorno de chamada que manipula o menu (LPFNDFMCALLBACK) para invocar um comando de menu.
title: Mensagem de DFM_INVOKECOMMAND (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967335"
---
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="ed4e7-103">\_Mensagem DFM INVOKECOMMAND</span><span class="sxs-lookup"><span data-stu-id="ed4e7-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="ed4e7-104">Enviado pela implementação do menu de contexto padrão para solicitar a função de retorno de chamada que manipula o menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) para invocar um comando de menu.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="ed4e7-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed4e7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed4e7-106">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ed4e7-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4e7-107">A ID de comando do comando de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="ed4e7-108">Os seguintes sinalizadores são reconhecidos:</span><span class="sxs-lookup"><span data-stu-id="ed4e7-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="ed4e7-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-110">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-110">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-111">Excluir o item atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="ed4e7-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_mover DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-113">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-113">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-114">Mover o item atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="ed4e7-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**cópia do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-116">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-116">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-117">Copiar o item atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="ed4e7-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**LINK do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-119">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-119">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-120">Crie um link para o item atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="ed4e7-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**Propriedades do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-122">Mostre a interface do usuário de **Propriedades** para o item no qual o menu foi invocado.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="ed4e7-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ cmd \_ NEWFOLDER**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-124">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="ed4e7-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_colar DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-126">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-126">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-127">Colar um item no local atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="ed4e7-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**exibição de DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-129">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="ed4e7-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM \_ cmd \_ VIEWDETAILS**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-131">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="ed4e7-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ cmd \_ PASTELINK**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-133">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-133">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-134">Cole um link no local atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="ed4e7-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ cmd \_ PASTESPECIAL**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-136">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="ed4e7-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ cmd \_ MODALPROP**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-138">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="ed4e7-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**\_renomear DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="ed4e7-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="ed4e7-140">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-140">**Windows Vista and later**.</span></span> <span data-ttu-id="ed4e7-141">Renomear o item atual.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ed4e7-142">*argumentos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ed4e7-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed4e7-143">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém argumentos adicionais para o comando de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="ed4e7-144">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed4e7-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed4e7-145">Return value</span></span>

<span data-ttu-id="ed4e7-146">O manipulador para essa mensagem precisa retornar S \_ false se você quiser que a implementação padrão invoque o manipulador padrão para o comando.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="ed4e7-147">Retorne \_ os S ok se a mensagem foi tratada.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="ed4e7-148">Caso contrário, retorne um código de erro HRESULT padrão.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed4e7-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed4e7-149">Remarks</span></span>

<span data-ttu-id="ed4e7-150">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o retorno de chamada é implementado.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="ed4e7-151">Há duas APIs para a construção de retorno de chamada, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) que usa um ponteiro para uma função de retorno de chamada ou [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) que usa um objeto de retorno de chamada que dá suporte a [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="ed4e7-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="ed4e7-152">Os itens nos quais o comando está sendo invocado são fornecidos em um objeto de dados passado para a função de retorno de chamada ou para o método [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="ed4e7-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="ed4e7-153">Esse objeto de dados é fornecido pela fonte de dados que implementa o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="ed4e7-154">Para extrair os itens do objeto de dados, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="ed4e7-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="ed4e7-155">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="ed4e7-156">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="ed4e7-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4e7-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed4e7-157">Requirements</span></span>



| <span data-ttu-id="ed4e7-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed4e7-158">Requirement</span></span> | <span data-ttu-id="ed4e7-159">Valor</span><span class="sxs-lookup"><span data-stu-id="ed4e7-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4e7-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed4e7-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ed4e7-161">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed4e7-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ed4e7-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed4e7-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ed4e7-163">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed4e7-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed4e7-164">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed4e7-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed4e7-165"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed4e7-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
