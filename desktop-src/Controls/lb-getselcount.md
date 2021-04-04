---
title: Mensagem de LB_GETSELCOUNT (WinUser. h)
description: Obtém o número total de itens selecionados em uma caixa de listagem de seleção múltipla.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- Controles de LB_GETSELCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085407"
---
# <a name="lb_getselcount-message"></a><span data-ttu-id="4a362-104">GETSELCOUNT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="4a362-104">LB\_GETSELCOUNT message</span></span>

<span data-ttu-id="4a362-105">Obtém o número total de itens selecionados em uma caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="4a362-105">Gets the total number of selected items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a362-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a362-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a362-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a362-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a362-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4a362-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a362-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a362-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a362-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4a362-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a362-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a362-111">Return value</span></span>

<span data-ttu-id="4a362-112">O valor de retorno é a contagem de itens selecionados na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="4a362-112">The return value is the count of selected items in the list box.</span></span> <span data-ttu-id="4a362-113">Se a caixa de listagem for uma caixa de listagem de seleção única, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="4a362-113">If the list box is a single-selection list box, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a362-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a362-114">Requirements</span></span>



| <span data-ttu-id="4a362-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a362-115">Requirement</span></span> | <span data-ttu-id="4a362-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4a362-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a362-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a362-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a362-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a362-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4a362-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a362-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a362-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a362-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a362-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a362-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a362-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a362-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a362-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a362-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a362-124">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="4a362-124">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> </dl>

 

 





