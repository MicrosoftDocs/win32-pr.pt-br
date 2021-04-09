---
title: Mensagem de LB_GETCURSEL (WinUser. h)
description: Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Controles de LB_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009713"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="48560-104">\_Mensagem GETcurseal de lb</span><span class="sxs-lookup"><span data-stu-id="48560-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="48560-105">Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="48560-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="48560-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48560-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48560-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48560-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48560-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="48560-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="48560-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48560-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48560-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="48560-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48560-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48560-111">Return value</span></span>

<span data-ttu-id="48560-112">Em uma caixa de listagem de seleção única, o valor de retorno é o índice de base zero do item selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="48560-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="48560-113">Se não houver nenhuma seleção, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="48560-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="48560-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="48560-114">Remarks</span></span>

<span data-ttu-id="48560-115">Para recuperar os índices dos itens selecionados em uma caixa de listagem de seleção múltipla, use a [**mensagem \_ GETSELITEMS de lb**](lb-getselitems.md) .</span><span class="sxs-lookup"><span data-stu-id="48560-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="48560-116">Para determinar se o item que tem o retângulo de foco em uma caixa de listagem de seleção múltipla está selecionado, use a mensagem [**\_ GETSEL de lb**](lb-getsel.md) .</span><span class="sxs-lookup"><span data-stu-id="48560-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="48560-117">Se for enviado para uma caixa de listagem de seleção múltipla, **lb \_ getcurseal** retornará o índice do item que tem o retângulo de foco.</span><span class="sxs-lookup"><span data-stu-id="48560-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="48560-118">Se nenhum item for selecionado, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="48560-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="48560-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48560-119">Requirements</span></span>



| <span data-ttu-id="48560-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48560-120">Requirement</span></span> | <span data-ttu-id="48560-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48560-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48560-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48560-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48560-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48560-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48560-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48560-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48560-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48560-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48560-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48560-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="48560-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48560-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48560-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="48560-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="48560-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="48560-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="48560-130">**\_GETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="48560-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="48560-131">**\_GETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="48560-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="48560-132">**\_GETSELITEMS lb**</span><span class="sxs-lookup"><span data-stu-id="48560-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="48560-133">**LB- \_ REcursel**</span><span class="sxs-lookup"><span data-stu-id="48560-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





