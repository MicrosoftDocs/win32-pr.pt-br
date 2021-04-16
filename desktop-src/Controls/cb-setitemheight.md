---
title: Mensagem de CB_SETITEMHEIGHT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETITEMHEIGHT CB para definir a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- Controles de CB_SETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750944"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="499ad-104">\_Mensagem de SETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="499ad-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="499ad-105">Um aplicativo envia uma mensagem de **\_ SETITEMHEIGHT CB** para definir a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="499ad-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="499ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="499ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="499ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="499ad-108">Especifica o componente da caixa de combinação para a qual definir a altura.</span><span class="sxs-lookup"><span data-stu-id="499ad-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="499ad-109">Esse parâmetro deve ser 1 para definir a altura do campo de seleção.</span><span class="sxs-lookup"><span data-stu-id="499ad-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="499ad-110">Ele deve ser zero para definir a altura dos itens de lista, a menos que a caixa de combinação tenha o estilo [**\_ OwnerDrawVariable do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="499ad-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="499ad-111">Nesse caso, o parâmetro *wParam* é o índice de base zero de um item de lista específico.</span><span class="sxs-lookup"><span data-stu-id="499ad-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="499ad-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="499ad-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="499ad-113">Especifica a altura, em pixels, do componente da caixa de combinação identificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="499ad-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499ad-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="499ad-114">Return value</span></span>

<span data-ttu-id="499ad-115">Se o índice ou a altura for inválido, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="499ad-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="499ad-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="499ad-116">Remarks</span></span>

<span data-ttu-id="499ad-117">A altura do campo de seleção em uma caixa de combinação é definida independentemente da altura dos itens da lista.</span><span class="sxs-lookup"><span data-stu-id="499ad-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="499ad-118">Um aplicativo deve garantir que a altura do campo de seleção não seja menor do que a altura de um item de lista específico.</span><span class="sxs-lookup"><span data-stu-id="499ad-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="499ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="499ad-119">Requirements</span></span>



| <span data-ttu-id="499ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="499ad-120">Requirement</span></span> | <span data-ttu-id="499ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="499ad-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="499ad-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="499ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="499ad-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="499ad-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="499ad-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="499ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="499ad-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="499ad-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="499ad-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="499ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="499ad-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="499ad-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="499ad-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="499ad-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="499ad-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="499ad-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="499ad-130">**\_GETITEMHEIGHT CB**</span><span class="sxs-lookup"><span data-stu-id="499ad-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="499ad-131">**MEASUREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="499ad-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





