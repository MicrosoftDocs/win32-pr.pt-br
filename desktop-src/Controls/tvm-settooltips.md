---
title: Mensagem de TVM_SETTOOLTIPS (commctrl. h)
description: Define um controle de dica de ferramenta filho do controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetToolTips de TreeView.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Controles de TVM_SETTOOLTIPS de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085535"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="0c965-105">\_Mensagem TVM SETtooltips</span><span class="sxs-lookup"><span data-stu-id="0c965-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="0c965-106">Define um controle de dica de ferramenta filho do controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="0c965-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="0c965-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetToolTips de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="0c965-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c965-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c965-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c965-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c965-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c965-110">Identificador para um controle de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="0c965-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="0c965-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c965-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0c965-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c965-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c965-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c965-113">Return value</span></span>

<span data-ttu-id="0c965-114">Retorna o identificador para o controle de dica de ferramenta definido anteriormente para o controle de exibição em árvore ou **NULL** se as dicas de ferramentas não foram usadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0c965-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c965-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c965-115">Remarks</span></span>

<span data-ttu-id="0c965-116">Quando criados, os controles de exibição de árvore criam automaticamente um controle de dica de ferramenta filho.</span><span class="sxs-lookup"><span data-stu-id="0c965-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="0c965-117">Para impedir que um controle de exibição de árvore use dicas de ferramenta, crie o controle com o estilo [**\_ notooltips de TVs**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0c965-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c965-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c965-118">Requirements</span></span>



| <span data-ttu-id="0c965-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c965-119">Requirement</span></span> | <span data-ttu-id="0c965-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0c965-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c965-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c965-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c965-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c965-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c965-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c965-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c965-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0c965-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c965-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c965-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c965-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c965-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c965-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c965-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c965-128">**\_GETtooltips TVM**</span><span class="sxs-lookup"><span data-stu-id="0c965-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





