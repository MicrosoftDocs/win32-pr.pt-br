---
title: Mensagem de LB_SELITEMRANGE (WinUser. h)
description: Seleciona ou anula a seleção de um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Controles de LB_SELITEMRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009656"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="b6185-104">SELITEMRANGE de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="b6185-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="b6185-105">Seleciona ou anula a seleção de um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="b6185-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6185-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6185-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6185-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6185-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6185-108">**True** para selecionar o intervalo de itens ou **false** para desselecioná-lo.</span><span class="sxs-lookup"><span data-stu-id="b6185-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="b6185-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6185-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6185-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice de base zero do primeiro item a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="b6185-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="b6185-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o índice de base zero do último item a ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="b6185-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6185-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6185-112">Return value</span></span>

<span data-ttu-id="b6185-113">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="b6185-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6185-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6185-114">Remarks</span></span>

<span data-ttu-id="b6185-115">Use essa mensagem somente com caixas de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="b6185-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="b6185-116">Esta mensagem pode selecionar um intervalo somente dentro dos primeiros 65.536 itens.</span><span class="sxs-lookup"><span data-stu-id="b6185-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6185-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6185-117">Requirements</span></span>



| <span data-ttu-id="b6185-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6185-118">Requirement</span></span> | <span data-ttu-id="b6185-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b6185-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6185-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6185-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6185-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6185-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6185-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6185-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6185-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6185-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6185-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6185-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6185-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6185-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6185-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6185-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6185-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b6185-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6185-128">**\_SELITEMRANGEEX lb**</span><span class="sxs-lookup"><span data-stu-id="b6185-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="b6185-129">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="b6185-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="b6185-130">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="b6185-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b6185-131">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="b6185-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

