---
title: Mensagem de LB_GETCARETINDEX (WinUser. h)
description: Recupera o índice do item que tem o foco em uma caixa de listagem de seleção múltipla. O item pode ou não ser selecionado.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Controles de LB_GETCARETINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009714"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="6fcd1-105">GETCARETINDEX de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="6fcd1-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="6fcd1-106">Recupera o índice do item que tem o foco em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="6fcd1-107">O item pode ou não ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fcd1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fcd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fcd1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fcd1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fcd1-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6fcd1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fcd1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fcd1-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fcd1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fcd1-113">Return value</span></span>

<span data-ttu-id="6fcd1-114">O valor de retorno é o índice de base zero do item da caixa de listagem focada ou 0 se nenhum item tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fcd1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fcd1-115">Remarks</span></span>

<span data-ttu-id="6fcd1-116">Essa mensagem também pode ser usada para obter o índice do item selecionado atualmente em uma caixa de listagem de seleção única.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcd1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fcd1-117">Requirements</span></span>



| <span data-ttu-id="6fcd1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcd1-118">Requirement</span></span> | <span data-ttu-id="6fcd1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6fcd1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcd1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fcd1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcd1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fcd1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6fcd1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fcd1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcd1-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fcd1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fcd1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fcd1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fcd1-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fcd1-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fcd1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fcd1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fcd1-127">**\_SETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="6fcd1-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





