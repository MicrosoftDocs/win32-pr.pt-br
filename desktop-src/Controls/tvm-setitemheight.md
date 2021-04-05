---
title: Mensagem de TVM_SETITEMHEIGHT (commctrl. h)
description: Define a altura dos itens de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetItemHeight.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Controles de TVM_SETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918611"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="c936f-105">\_Mensagem TVM SETITEMHEIGHT</span><span class="sxs-lookup"><span data-stu-id="c936f-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="c936f-106">Define a altura dos itens de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="c936f-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="c936f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .</span><span class="sxs-lookup"><span data-stu-id="c936f-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c936f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c936f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c936f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c936f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c936f-110">Nova altura de cada item no modo de exibição de árvore, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c936f-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="c936f-111">As alturas inferiores a 1 serão definidas como 1.</span><span class="sxs-lookup"><span data-stu-id="c936f-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="c936f-112">Se esse argumento não for par e o controle de exibição de árvore não tiver o estilo de [**TVs \_ NONEVENHEIGHT**](tree-view-control-window-styles.md) , esse valor será arredondado para baixo até o valor par mais próximo.</span><span class="sxs-lookup"><span data-stu-id="c936f-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="c936f-113">Se esse argumento for-1, o controle será revertido para usar sua altura de item padrão.</span><span class="sxs-lookup"><span data-stu-id="c936f-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="c936f-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c936f-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c936f-115">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c936f-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c936f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c936f-116">Return value</span></span>

<span data-ttu-id="c936f-117">Retorna a altura anterior dos itens, em pixels.</span><span class="sxs-lookup"><span data-stu-id="c936f-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="c936f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c936f-118">Remarks</span></span>

<span data-ttu-id="c936f-119">O controle de exibição de árvore usa esse valor para a altura de todos os itens.</span><span class="sxs-lookup"><span data-stu-id="c936f-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="c936f-120">Para modificar a altura de itens individuais, consulte a descrição do membro **iIntegral** da estrutura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="c936f-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c936f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c936f-121">Requirements</span></span>



| <span data-ttu-id="c936f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c936f-122">Requirement</span></span> | <span data-ttu-id="c936f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c936f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c936f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c936f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c936f-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c936f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c936f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c936f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c936f-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c936f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c936f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c936f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c936f-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c936f-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c936f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c936f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c936f-131">**TVM \_ GETITEMHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="c936f-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





