---
title: Mensagem de LB_SELITEMRANGEEX (WinUser. h)
description: Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Controles de LB_SELITEMRANGEEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918980"
---
# <a name="lb_selitemrangeex-message"></a><span data-ttu-id="e7afc-104">SELITEMRANGEEX de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="e7afc-104">LB\_SELITEMRANGEEX message</span></span>

<span data-ttu-id="e7afc-105">Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="e7afc-105">Selects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7afc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7afc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7afc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7afc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7afc-108">Especifica o índice de base zero do primeiro item a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="e7afc-108">Specifies the zero-based index of the first item to select.</span></span>

<span data-ttu-id="e7afc-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e7afc-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="e7afc-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="e7afc-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="e7afc-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="e7afc-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="e7afc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7afc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7afc-113">Especifica o índice de base zero do último item a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="e7afc-113">Specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7afc-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7afc-114">Return value</span></span>

<span data-ttu-id="e7afc-115">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="e7afc-115">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7afc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7afc-116">Remarks</span></span>

<span data-ttu-id="e7afc-117">Se o parâmetro *wParam* for menor que o parâmetro *lParam* , o intervalo de itens especificado será selecionado.</span><span class="sxs-lookup"><span data-stu-id="e7afc-117">If the *wParam* parameter is less than the *lParam* parameter, the specified range of items is selected.</span></span> <span data-ttu-id="e7afc-118">Se *wParam* for maior ou igual a *lParam*, o intervalo será removido do intervalo de itens especificado.</span><span class="sxs-lookup"><span data-stu-id="e7afc-118">If *wParam* is greater than or equal to *lParam*, the range is removed from the specified range of items.</span></span> <span data-ttu-id="e7afc-119">Para selecionar apenas um item, selecione dois itens e, em seguida, desmarque o item indesejado.</span><span class="sxs-lookup"><span data-stu-id="e7afc-119">To select only one item, select two items and then deselect the unwanted item.</span></span>

<span data-ttu-id="e7afc-120">Use essa mensagem somente com caixas de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="e7afc-120">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="e7afc-121">Esta mensagem pode selecionar um intervalo somente dentro dos primeiros 65.536 itens.</span><span class="sxs-lookup"><span data-stu-id="e7afc-121">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7afc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7afc-122">Requirements</span></span>



| <span data-ttu-id="e7afc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7afc-123">Requirement</span></span> | <span data-ttu-id="e7afc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e7afc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7afc-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7afc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7afc-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7afc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7afc-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7afc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7afc-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7afc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7afc-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7afc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7afc-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7afc-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7afc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7afc-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7afc-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e7afc-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7afc-133">**\_SELITEMRANGE lb**</span><span class="sxs-lookup"><span data-stu-id="e7afc-133">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> <dt>

[<span data-ttu-id="e7afc-134">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="e7afc-134">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





