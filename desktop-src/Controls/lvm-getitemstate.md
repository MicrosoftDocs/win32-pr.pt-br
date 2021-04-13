---
title: Mensagem de LVM_GETITEMSTATE (commctrl. h)
description: Recupera o estado de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemState do ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Controles de LVM_GETITEMSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455747"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="cf1b3-105">Mensagem do LVM \_ GETitemstate</span><span class="sxs-lookup"><span data-stu-id="cf1b3-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="cf1b3-106">Recupera o estado de um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="cf1b3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemState do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="cf1b3-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf1b3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf1b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf1b3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf1b3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf1b3-110">Índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="cf1b3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf1b3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf1b3-112">Informações de estado a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-112">State information to retrieve.</span></span> <span data-ttu-id="cf1b3-113">Esse parâmetro pode ser uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="cf1b3-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="cf1b3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cf1b3-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="cf1b3-115">Significado</span><span class="sxs-lookup"><span data-stu-id="cf1b3-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="cf1b3-116"><dt>**LVIS \_ recortar**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="cf1b3-117">O item é marcado para uma operação de recortar e colar.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="cf1b3-118"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="cf1b3-119">O item é realçado como um destino do tipo "arrastar e soltar".</span><span class="sxs-lookup"><span data-stu-id="cf1b3-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="cf1b3-120"><dt>**LVIS com \_ foco**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="cf1b3-121">O item tem o foco, portanto, está circundado por um retângulo de foco padrão.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="cf1b3-122">Embora mais de um item possa ser selecionado, somente um item pode ter o foco.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="cf1b3-123"><dt>**LVIS \_ selecionado**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="cf1b3-124">O item está selecionado.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-124">The item is selected.</span></span> <span data-ttu-id="cf1b3-125">A aparência de um item selecionado depende de se ele tem o foco e também das cores do sistema usadas para seleção.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="cf1b3-126"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="cf1b3-127">Use essa máscara para recuperar o índice de imagem de sobreposição do item.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="cf1b3-128"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="cf1b3-129">Use essa máscara para recuperar o índice de imagem de estado do item.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf1b3-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf1b3-130">Return value</span></span>

<span data-ttu-id="cf1b3-131">Retorna o estado atual do item especificado.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="cf1b3-132">Os únicos bits válidos no valor de retorno são aqueles que correspondem aos bits definidos no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cf1b3-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf1b3-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf1b3-133">Remarks</span></span>

<span data-ttu-id="cf1b3-134">As informações de estado de um item incluem um conjunto de sinalizadores de bit, bem como índices de lista de imagens que indicam a imagem de estado e a imagem de sobreposição do item.</span><span class="sxs-lookup"><span data-stu-id="cf1b3-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf1b3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf1b3-135">Requirements</span></span>



| <span data-ttu-id="cf1b3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf1b3-136">Requirement</span></span> | <span data-ttu-id="cf1b3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="cf1b3-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1b3-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf1b3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cf1b3-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf1b3-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf1b3-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf1b3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cf1b3-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf1b3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf1b3-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf1b3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf1b3-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf1b3-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf1b3-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf1b3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1b3-145">**GetItemState do LVM \_**</span><span class="sxs-lookup"><span data-stu-id="cf1b3-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 





