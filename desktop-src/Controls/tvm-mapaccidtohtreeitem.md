---
title: Mensagem de TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Mapeia uma ID de acessibilidade para um HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Controles de TVM_MAPACCIDTOHTREEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009106"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="fe541-104">\_Mensagem TVM MAPACCIDTOHTREEITEM</span><span class="sxs-lookup"><span data-stu-id="fe541-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="fe541-105">Mapeia uma ID de acessibilidade para um **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="fe541-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe541-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe541-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe541-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe541-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe541-108">**Uint** que contém a ID de acessibilidade para mapear para um **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="fe541-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="fe541-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe541-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fe541-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fe541-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe541-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe541-111">Return value</span></span>

<span data-ttu-id="fe541-112">Retorna o **HTREEITEM** ao qual a ID de acessibilidade especificada está mapeada.</span><span class="sxs-lookup"><span data-stu-id="fe541-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe541-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe541-113">Remarks</span></span>

<span data-ttu-id="fe541-114">Quando você adiciona um item a um controle de exibição de árvore, um **HTREEITEM** retorna, que identifica exclusivamente o item.</span><span class="sxs-lookup"><span data-stu-id="fe541-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="fe541-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="fe541-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fe541-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fe541-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe541-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe541-117">Requirements</span></span>



| <span data-ttu-id="fe541-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe541-118">Requirement</span></span> | <span data-ttu-id="fe541-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fe541-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe541-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe541-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe541-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe541-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe541-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe541-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe541-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe541-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe541-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe541-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe541-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe541-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe541-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe541-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe541-127">**\_MapAccIDToHTREEITEM TreeView**</span><span class="sxs-lookup"><span data-stu-id="fe541-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





