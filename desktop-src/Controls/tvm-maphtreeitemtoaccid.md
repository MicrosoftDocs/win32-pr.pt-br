---
title: Mensagem de TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Mapeia um HTREEITEM para uma ID de acessibilidade.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Controles de TVM_MAPHTREEITEMTOACCID de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085569"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="3707a-104">\_Mensagem TVM MAPHTREEITEMTOACCID</span><span class="sxs-lookup"><span data-stu-id="3707a-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="3707a-105">Mapeia um **HTREEITEM** para uma ID de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="3707a-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="3707a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3707a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3707a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3707a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3707a-108">**HTREEITEM** que é mapeado para uma ID de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="3707a-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="3707a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3707a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3707a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3707a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3707a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3707a-111">Return value</span></span>

<span data-ttu-id="3707a-112">Retorna uma ID de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="3707a-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="3707a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3707a-113">Remarks</span></span>

<span data-ttu-id="3707a-114">Quando você adiciona um item a um controle de exibição de árvore, um identificador **HTREEITEM** é retornado para identificar exclusivamente o item.</span><span class="sxs-lookup"><span data-stu-id="3707a-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="3707a-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3707a-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="3707a-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3707a-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3707a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3707a-117">Requirements</span></span>



| <span data-ttu-id="3707a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3707a-118">Requirement</span></span> | <span data-ttu-id="3707a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3707a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3707a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3707a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3707a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3707a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3707a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3707a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3707a-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3707a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3707a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3707a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3707a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3707a-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3707a-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3707a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3707a-127">**\_MapHTREEITEMtoAccID TreeView**</span><span class="sxs-lookup"><span data-stu-id="3707a-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





