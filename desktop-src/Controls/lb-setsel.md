---
title: Mensagem de LB_SETSEL (WinUser. h)
description: Seleciona um item em uma caixa de listagem de seleção múltipla e, se necessário, rola o item para a exibição.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Controles de LB_SETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455753"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="657e3-104">SETSEL de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="657e3-104">LB\_SETSEL message</span></span>

<span data-ttu-id="657e3-105">Seleciona um item em uma caixa de listagem de seleção múltipla e, se necessário, rola o item para a exibição.</span><span class="sxs-lookup"><span data-stu-id="657e3-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="657e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="657e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="657e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="657e3-108">Especifica como definir a seleção.</span><span class="sxs-lookup"><span data-stu-id="657e3-108">Specifies how to set the selection.</span></span> <span data-ttu-id="657e3-109">Se esse parâmetro for **true**, o item será selecionado e realçado; Se for **false**, o realce será removido e o item não será mais selecionado.</span><span class="sxs-lookup"><span data-stu-id="657e3-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="657e3-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="657e3-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="657e3-111">Especifica o índice de base zero do item a ser definido.</span><span class="sxs-lookup"><span data-stu-id="657e3-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="657e3-112">Se esse parâmetro for-1, a seleção será adicionada ou removida de todos os itens, dependendo do valor de *wParam*, e não ocorrerá nenhuma rolagem.</span><span class="sxs-lookup"><span data-stu-id="657e3-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657e3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="657e3-113">Return value</span></span>

<span data-ttu-id="657e3-114">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="657e3-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="657e3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="657e3-115">Remarks</span></span>

<span data-ttu-id="657e3-116">Use essa mensagem somente com caixas de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="657e3-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="657e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="657e3-117">Requirements</span></span>



| <span data-ttu-id="657e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="657e3-118">Requirement</span></span> | <span data-ttu-id="657e3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="657e3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="657e3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="657e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="657e3-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="657e3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="657e3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="657e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="657e3-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="657e3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="657e3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="657e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="657e3-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="657e3-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="657e3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="657e3-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="657e3-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="657e3-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="657e3-128">**\_GETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="657e3-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="657e3-129">**\_SELITEMRANGE lb**</span><span class="sxs-lookup"><span data-stu-id="657e3-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





