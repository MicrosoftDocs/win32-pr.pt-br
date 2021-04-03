---
title: Mensagem de LB_SETCARETINDEX (WinUser. h)
description: Define o retângulo de foco para o item no índice especificado em uma caixa de listagem de seleção múltipla. Se o item não estiver visível, ele será rolado para a exibição.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Controles de LB_SETCARETINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824678"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="c649b-105">SETCARETINDEX de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="c649b-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="c649b-106">Define o retângulo de foco para o item no índice especificado em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="c649b-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="c649b-107">Se o item não estiver visível, ele será rolado para a exibição.</span><span class="sxs-lookup"><span data-stu-id="c649b-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="c649b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c649b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c649b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c649b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c649b-110">Especifica o índice de base zero do item da caixa de listagem que deve receber o retângulo de foco.</span><span class="sxs-lookup"><span data-stu-id="c649b-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="c649b-111">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c649b-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="c649b-112">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="c649b-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="c649b-113">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="c649b-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="c649b-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c649b-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c649b-115">Se esse valor for **false**, o item será rolado até que fique totalmente visível; Se for **true**, o item será rolado até que seja pelo menos parcialmente visível.</span><span class="sxs-lookup"><span data-stu-id="c649b-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c649b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c649b-116">Return value</span></span>

<span data-ttu-id="c649b-117">Se ocorrer um erro, o valor de retorno será um erro de LB \_ (-1).</span><span class="sxs-lookup"><span data-stu-id="c649b-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="c649b-118">Caso contrário, LB \_ OK (0) será retornado.</span><span class="sxs-lookup"><span data-stu-id="c649b-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c649b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c649b-119">Remarks</span></span>

<span data-ttu-id="c649b-120">Se essa mensagem for enviada para uma caixa de listagem de seleção única que não contém um item selecionado, o índice de cursor será definido como o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c649b-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="c649b-121">Se a caixa de listagem de seleção única contiver um item selecionado, a caixa de listagem retornará um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="c649b-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="c649b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c649b-122">Requirements</span></span>



| <span data-ttu-id="c649b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c649b-123">Requirement</span></span> | <span data-ttu-id="c649b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c649b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c649b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c649b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c649b-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c649b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c649b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c649b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c649b-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c649b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c649b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c649b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c649b-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c649b-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c649b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c649b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c649b-132">**\_GETCARETINDEX lb**</span><span class="sxs-lookup"><span data-stu-id="c649b-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





