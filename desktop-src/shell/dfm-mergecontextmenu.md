---
description: Permite que o retorno de chamada adicione itens ao menu.
title: Mensagem de DFM_MERGECONTEXTMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d469f9764b5e377e5f47227d3414f246441d3505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967331"
---
# <a name="dfm_mergecontextmenu-message"></a><span data-ttu-id="09554-103">\_Mensagem DFM MERGECONTEXTMENU</span><span class="sxs-lookup"><span data-stu-id="09554-103">DFM\_MERGECONTEXTMENU message</span></span>

<span data-ttu-id="09554-104">Permite que o retorno de chamada adicione itens ao menu.</span><span class="sxs-lookup"><span data-stu-id="09554-104">Allows the callback to add items to the menu.</span></span>


```C++
DFM_MERGECONTEXTMENU

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="09554-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09554-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09554-106">*pqcminfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09554-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09554-107">Um ponteiro para uma estrutura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contém as informações usadas na mesclagem.</span><span class="sxs-lookup"><span data-stu-id="09554-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="09554-108">*uFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09554-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09554-109">Sinalizadores que especificam como o menu de contexto pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="09554-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="09554-110">Esse parâmetro usa os valores de CMF \_ \* descritos em [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="09554-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09554-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="09554-111">Remarks</span></span>

<span data-ttu-id="09554-112">Se os itens forem adicionados ao menu de contexto, eles deverão ter suporte com rotinas que respondem adequadamente quando um desses itens é invocado usando [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="09554-112">If items are added to the context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="09554-113">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é implementado.</span><span class="sxs-lookup"><span data-stu-id="09554-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="09554-114">Há duas APIs para sua implementação, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="09554-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="09554-115">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="09554-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="09554-116">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="09554-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="09554-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09554-117">Requirements</span></span>



| <span data-ttu-id="09554-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09554-118">Requirement</span></span> | <span data-ttu-id="09554-119">Valor</span><span class="sxs-lookup"><span data-stu-id="09554-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09554-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09554-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09554-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09554-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09554-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09554-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09554-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09554-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09554-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="09554-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="09554-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="09554-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




