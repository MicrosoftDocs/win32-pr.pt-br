---
title: Mensagem de TVM_SETIMAGELIST (commctrl. h)
description: Define a lista de imagens normal ou de estado para um controle de exibição em árvore e redesenha o controle usando as novas imagens. Você pode enviar essa mensagem explicitamente ou usando a macro do \_ Defaultimagelist de árvore.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Controles de TVM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644663"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="b6997-105">\_Mensagem TVM SETimagelist</span><span class="sxs-lookup"><span data-stu-id="b6997-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="b6997-106">Define a lista de imagens normal ou de estado para um controle de exibição em árvore e redesenha o controle usando as novas imagens.</span><span class="sxs-lookup"><span data-stu-id="b6997-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="b6997-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**do \_ defaultimagelist de árvore**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="b6997-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6997-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6997-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6997-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6997-110">Tipo de lista de imagens a ser definida.</span><span class="sxs-lookup"><span data-stu-id="b6997-110">Type of image list to set.</span></span> <span data-ttu-id="b6997-111">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b6997-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="b6997-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b6997-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="b6997-113">Significado</span><span class="sxs-lookup"><span data-stu-id="b6997-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="b6997-114"><dt>**TVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="b6997-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="b6997-115">Indica a lista de imagens normal, que contém imagens selecionadas, não selecionadas e sobreposição para os itens de um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="b6997-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="b6997-116"><dt>**\_estado TVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b6997-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="b6997-117">Indica a lista de imagens de estado.</span><span class="sxs-lookup"><span data-stu-id="b6997-117">Indicates the state image list.</span></span> <span data-ttu-id="b6997-118">Você pode usar imagens de estado para indicar os Estados de itens definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6997-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="b6997-119">Uma imagem de estado é exibida à esquerda da imagem selecionada ou não marcada de um item.</span><span class="sxs-lookup"><span data-stu-id="b6997-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b6997-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6997-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6997-121">Identificador para a lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="b6997-121">Handle to the image list.</span></span> <span data-ttu-id="b6997-122">Se *lParam* for **NULL**, a mensagem removerá a lista de imagens especificada do controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="b6997-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6997-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6997-123">Return value</span></span>

<span data-ttu-id="b6997-124">Retorna o identificador para a lista de imagens anterior, se houver, ou **NULL** de outra forma.</span><span class="sxs-lookup"><span data-stu-id="b6997-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6997-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6997-125">Remarks</span></span>

<span data-ttu-id="b6997-126">O controle de exibição de árvore não destruirá a lista de imagens especificada com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="b6997-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="b6997-127">Seu aplicativo deve destruir a lista de imagens quando ela não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="b6997-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6997-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6997-128">Requirements</span></span>



| <span data-ttu-id="b6997-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6997-129">Requirement</span></span> | <span data-ttu-id="b6997-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b6997-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6997-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6997-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b6997-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6997-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6997-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6997-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b6997-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6997-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6997-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6997-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6997-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6997-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6997-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6997-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6997-138">**TVM \_ GETimagelist**</span><span class="sxs-lookup"><span data-stu-id="b6997-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 





