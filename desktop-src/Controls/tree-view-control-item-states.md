---
title: Estados do item de controle de Tree-View (CommCtrl. h)
description: Esta seção lista os sinalizadores de estado do item usados para indicar o estado de um item em um controle de exibição de árvore.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769026"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="0c671-103">Tree-View Estados de item de controle</span><span class="sxs-lookup"><span data-stu-id="0c671-103">Tree-View Control Item States</span></span>

<span data-ttu-id="0c671-104">Esta seção lista os sinalizadores de estado do item usados para indicar o estado de um item em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="0c671-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="0c671-105">Constante</span><span class="sxs-lookup"><span data-stu-id="0c671-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="0c671-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c671-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="0c671-107"><dt>**TVIS \_ bold**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="0c671-108">O item está em negrito.</span><span class="sxs-lookup"><span data-stu-id="0c671-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="0c671-109"><dt>**TVIS \_ recortar**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="0c671-110">O item é selecionado como parte de uma operação de recortar e colar.</span><span class="sxs-lookup"><span data-stu-id="0c671-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="0c671-111"><dt>**TVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="0c671-112">O item é selecionado como um destino de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="0c671-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="0c671-113"><dt>**TVIS \_ expandido**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="0c671-114">A lista de itens filhos do item está expandida no momento; ou seja, os itens filho são visíveis.</span><span class="sxs-lookup"><span data-stu-id="0c671-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="0c671-115">Esse valor se aplica somente a itens pai.</span><span class="sxs-lookup"><span data-stu-id="0c671-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="0c671-116"><dt>**TVIS \_ EXPANDEDONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="0c671-117">A lista de itens filho do item foi expandida pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="0c671-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="0c671-118">Os códigos de notificação [TVN \_ doexpanding](tvn-itemexpanding.md) e TVN item- [ \_ Expanded](tvn-itemexpanded.md) não são gerados para itens pai que têm esse estado definido em resposta a uma mensagem de [**\_ expansão TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="0c671-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="0c671-119">Usar TVE \_ Collapse e TVE \_ COLLAPSERESET com **TVM \_ Expand** fará com que esse Estado seja redefinido.</span><span class="sxs-lookup"><span data-stu-id="0c671-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="0c671-120">Esse valor se aplica somente a itens pai.</span><span class="sxs-lookup"><span data-stu-id="0c671-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="0c671-121"><dt>**TVIS \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="0c671-122">**Versão 4,70**.</span><span class="sxs-lookup"><span data-stu-id="0c671-122">**Version 4.70**.</span></span> <span data-ttu-id="0c671-123">Um item de exibição de árvore parcialmente expandido.</span><span class="sxs-lookup"><span data-stu-id="0c671-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="0c671-124">Nesse estado, alguns, mas não todos, os itens filho são visíveis e o símbolo de adição do item pai é exibido.</span><span class="sxs-lookup"><span data-stu-id="0c671-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="0c671-125"><dt>**TVIS \_ selecionado**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="0c671-126">O item está selecionado.</span><span class="sxs-lookup"><span data-stu-id="0c671-126">The item is selected.</span></span> <span data-ttu-id="0c671-127">Sua aparência depende de se ele tem o foco.</span><span class="sxs-lookup"><span data-stu-id="0c671-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="0c671-128">O item será desenhado usando as cores do sistema para seleção.</span><span class="sxs-lookup"><span data-stu-id="0c671-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="0c671-129"><dt>**TVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="0c671-130">Máscara para os bits usados para especificar o índice de imagem de sobreposição do item.</span><span class="sxs-lookup"><span data-stu-id="0c671-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="0c671-131"><dt>**TVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="0c671-132">Máscara para os bits usados para especificar o índice de imagem de estado do item.</span><span class="sxs-lookup"><span data-stu-id="0c671-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="0c671-133"><dt>**usermask TVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="0c671-134">O mesmo que **TVIS \_ STATEIMAGEMASK**.</span><span class="sxs-lookup"><span data-stu-id="0c671-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="0c671-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c671-135">Remarks</span></span>

<span data-ttu-id="0c671-136">Quando você define ou recupera um índice de imagem de sobreposição de um item ou um índice de imagem de estado, você deve especificar as seguintes máscaras no membro **stateMask** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :</span><span class="sxs-lookup"><span data-stu-id="0c671-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="0c671-137">**TVIS \_ OVERLAYMASK**</span><span class="sxs-lookup"><span data-stu-id="0c671-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="0c671-138">**TVIS \_ STATEIMAGEMASK**</span><span class="sxs-lookup"><span data-stu-id="0c671-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="0c671-139">**usermask TVIS \_**</span><span class="sxs-lookup"><span data-stu-id="0c671-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="0c671-140">Esses valores também podem ser usados para mascarar os bits de estado que não são de interesse.</span><span class="sxs-lookup"><span data-stu-id="0c671-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c671-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c671-141">Requirements</span></span>



| <span data-ttu-id="0c671-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c671-142">Requirement</span></span> | <span data-ttu-id="0c671-143">Valor</span><span class="sxs-lookup"><span data-stu-id="0c671-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c671-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c671-144">Header</span></span><br/> | <dl> <span data-ttu-id="0c671-145"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





