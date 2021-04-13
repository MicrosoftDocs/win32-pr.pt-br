---
title: Mensagem de TVM_GETTOOLTIPS (commctrl. h)
description: Recupera o identificador para o controle ToolTip filho usado por um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetToolTips do TreeView.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Controles de TVM_GETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454873"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="50f1a-105">\_Mensagem TVM GETtooltips</span><span class="sxs-lookup"><span data-stu-id="50f1a-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="50f1a-106">Recupera o identificador para o controle ToolTip filho usado por um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="50f1a-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="50f1a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetToolTips do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="50f1a-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="50f1a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50f1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50f1a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50f1a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="50f1a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="50f1a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="50f1a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50f1a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="50f1a-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="50f1a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50f1a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50f1a-113">Return value</span></span>

<span data-ttu-id="50f1a-114">Retorna o identificador para o controle ToolTip filho ou **NULL** se o controle não estiver usando dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="50f1a-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f1a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="50f1a-115">Remarks</span></span>

<span data-ttu-id="50f1a-116">Quando criados, os controles de exibição de árvore criam automaticamente um controle de dica de ferramenta filho.</span><span class="sxs-lookup"><span data-stu-id="50f1a-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="50f1a-117">Para fazer com que um controle de exibição em árvore não use dicas de ferramenta, crie o controle com o estilo [**\_ notooltips de TVs**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="50f1a-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="50f1a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50f1a-118">Requirements</span></span>



| <span data-ttu-id="50f1a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50f1a-119">Requirement</span></span> | <span data-ttu-id="50f1a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="50f1a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50f1a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50f1a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="50f1a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50f1a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50f1a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50f1a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="50f1a-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50f1a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50f1a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50f1a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f1a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50f1a-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f1a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="50f1a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f1a-128">**TVM \_ SETtooltip**</span><span class="sxs-lookup"><span data-stu-id="50f1a-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





