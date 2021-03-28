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
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="1adc2-104">\_Mensagem DFM GETDEFSTATICID</span><span class="sxs-lookup"><span data-stu-id="1adc2-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="1adc2-105">Enviado pela implementação do menu de contexto padrão durante a criação, especificando o comando de menu padrão e permitindo que uma escolha alternativa seja feita.</span><span class="sxs-lookup"><span data-stu-id="1adc2-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="1adc2-106">Usado por [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span><span class="sxs-lookup"><span data-stu-id="1adc2-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="1adc2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1adc2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1adc2-108">*definição de padrão* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1adc2-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1adc2-109">Um ponteiro para a ID do comando de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="1adc2-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="1adc2-110">O sinalizador a seguir é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="1adc2-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="1adc2-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**Propriedades do DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="1adc2-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="1adc2-112">Mostrar a interface do usuário de **Propriedades** do item no qual o menu foi invocado.</span><span class="sxs-lookup"><span data-stu-id="1adc2-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1adc2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1adc2-113">Remarks</span></span>

<span data-ttu-id="1adc2-114">Para substituir a opção de comando padrão, seu manipulador deve, após o recebimento dessa mensagem, definir o valor apontado por *DefaultID* para a ID do comando de substituição e retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1adc2-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="1adc2-115">Caso contrário, retorna um código de falha.</span><span class="sxs-lookup"><span data-stu-id="1adc2-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="1adc2-116">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído.</span><span class="sxs-lookup"><span data-stu-id="1adc2-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="1adc2-117">Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="1adc2-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="1adc2-118">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="1adc2-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="1adc2-119">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="1adc2-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1adc2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1adc2-120">Requirements</span></span>



| <span data-ttu-id="1adc2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1adc2-121">Requirement</span></span> | <span data-ttu-id="1adc2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1adc2-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1adc2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1adc2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1adc2-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1adc2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1adc2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1adc2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1adc2-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1adc2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1adc2-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1adc2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1adc2-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1adc2-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
