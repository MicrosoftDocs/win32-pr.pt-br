---
title: Mensagem de LB_RESETCONTENT (WinUser. h)
description: Remove todos os itens de uma caixa de listagem.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- Controles de LB_RESETCONTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0091871df045812dcaa7a159cc456a1350d20f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824682"
---
# <a name="lb_resetcontent-message"></a><span data-ttu-id="0c05b-104">RESETCONTENT de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="0c05b-104">LB\_RESETCONTENT message</span></span>

<span data-ttu-id="0c05b-105">Remove todos os itens de uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0c05b-105">Removes all items from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c05b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c05b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c05b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c05b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c05b-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c05b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0c05b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c05b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c05b-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c05b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c05b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c05b-111">Return value</span></span>

<span data-ttu-id="0c05b-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0c05b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c05b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c05b-113">Remarks</span></span>

<span data-ttu-id="0c05b-114">Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o proprietário da caixa de listagem receberá uma mensagem do [**WM \_ DELETEITEM**](wm-deleteitem.md) para cada item na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0c05b-114">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the owner of the list box receives a [**WM\_DELETEITEM**](wm-deleteitem.md) message for each item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c05b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c05b-115">Requirements</span></span>



| <span data-ttu-id="0c05b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c05b-116">Requirement</span></span> | <span data-ttu-id="0c05b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0c05b-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c05b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c05b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0c05b-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c05b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0c05b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c05b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0c05b-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c05b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c05b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c05b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c05b-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c05b-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c05b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c05b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c05b-125">**DELETEITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="0c05b-125">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





