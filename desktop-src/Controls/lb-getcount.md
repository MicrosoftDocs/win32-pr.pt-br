---
title: Mensagem de LB_GETCOUNT (WinUser. h)
description: Obtém o número de itens em uma caixa de listagem.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- Controles de LB_GETCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddedbd7b9165e00e722edbadbb8806a68417551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455895"
---
# <a name="lb_getcount-message"></a><span data-ttu-id="7f3ba-104">\_Mensagem de GETcount de lb</span><span class="sxs-lookup"><span data-stu-id="7f3ba-104">LB\_GETCOUNT message</span></span>

<span data-ttu-id="7f3ba-105">Obtém o número de itens em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="7f3ba-105">Gets the number of items in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f3ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f3ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f3ba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f3ba-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3ba-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f3ba-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f3ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f3ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f3ba-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f3ba-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f3ba-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f3ba-111">Return value</span></span>

<span data-ttu-id="7f3ba-112">O valor de retorno é o número de itens na caixa de listagem, ou \_ erro de lb se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="7f3ba-112">The return value is the number of items in the list box, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f3ba-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f3ba-113">Remarks</span></span>

<span data-ttu-id="7f3ba-114">A contagem retornada é uma maior que o valor de índice do último item (o índice é baseado em zero).</span><span class="sxs-lookup"><span data-stu-id="7f3ba-114">The returned count is one greater than the index value of the last item (the index is zero-based).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3ba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f3ba-115">Requirements</span></span>



| <span data-ttu-id="7f3ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f3ba-116">Requirement</span></span> | <span data-ttu-id="7f3ba-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7f3ba-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3ba-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f3ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3ba-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f3ba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f3ba-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f3ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3ba-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f3ba-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f3ba-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f3ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f3ba-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f3ba-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f3ba-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f3ba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3ba-125">**NÚMERO de LB \_**</span><span class="sxs-lookup"><span data-stu-id="7f3ba-125">**LB\_SETCOUNT**</span></span>](lb-setcount.md)
</dt> </dl>

 

 





