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
ms.openlocfilehash: b9274a36f531e53f86d05adab20b4970ea5ace84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967333"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a><span data-ttu-id="48f50-103">Mensagem de DFM \_ MERGECONTEXTMENU \_ inferior</span><span class="sxs-lookup"><span data-stu-id="48f50-103">DFM\_MERGECONTEXTMENU\_BOTTOM message</span></span>

<span data-ttu-id="48f50-104">Permite que o retorno de chamada adicione itens à parte inferior do menu estendido.</span><span class="sxs-lookup"><span data-stu-id="48f50-104">Allows the callback to add items to the bottom of the extended menu.</span></span>


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="48f50-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48f50-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f50-106">*pqcminfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48f50-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48f50-107">Um ponteiro para uma estrutura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contém as informações usadas na mesclagem.</span><span class="sxs-lookup"><span data-stu-id="48f50-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="48f50-108">*uFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48f50-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48f50-109">Sinalizadores que especificam como o menu de contexto pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="48f50-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="48f50-110">Esse parâmetro usa os valores de CMF \_ \* descritos em [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="48f50-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48f50-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="48f50-111">Remarks</span></span>

<span data-ttu-id="48f50-112">Se os itens forem adicionados ao menu de contexto estendido, eles deverão ter suporte com rotinas que respondem adequadamente quando um desses itens é invocado usando [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="48f50-112">If items are added to the extended context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="48f50-113">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído.</span><span class="sxs-lookup"><span data-stu-id="48f50-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="48f50-114">Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="48f50-114">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="48f50-115">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="48f50-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="48f50-116">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="48f50-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f50-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48f50-117">Requirements</span></span>



| <span data-ttu-id="48f50-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="48f50-118">Requirement</span></span> | <span data-ttu-id="48f50-119">Valor</span><span class="sxs-lookup"><span data-stu-id="48f50-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48f50-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="48f50-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48f50-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="48f50-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="48f50-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48f50-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="48f50-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48f50-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="48f50-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="48f50-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




