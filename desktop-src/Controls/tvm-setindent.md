---
title: Mensagem de TVM_SETINDENT (commctrl. h)
description: Define a largura do recuo para um controle de exibição de árvore e redesenha o controle para refletir a nova largura. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetIndent de TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Controles de TVM_SETINDENT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085722"
---
# <a name="tvm_setindent-message"></a><span data-ttu-id="33579-105">Mensagem de TVM de \_ SUBrecuo</span><span class="sxs-lookup"><span data-stu-id="33579-105">TVM\_SETINDENT message</span></span>

<span data-ttu-id="33579-106">Define a largura do recuo para um controle de exibição de árvore e redesenha o controle para refletir a nova largura.</span><span class="sxs-lookup"><span data-stu-id="33579-106">Sets the width of indentation for a tree-view control and redraws the control to reflect the new width.</span></span> <span data-ttu-id="33579-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetIndent de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .</span><span class="sxs-lookup"><span data-stu-id="33579-107">You can send this message explicitly or by using the [**TreeView\_SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="33579-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33579-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33579-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33579-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33579-110">Largura, em pixels, do recuo.</span><span class="sxs-lookup"><span data-stu-id="33579-110">Width, in pixels, of the indentation.</span></span> <span data-ttu-id="33579-111">Se esse parâmetro for menor que a largura mínima definida pelo sistema, a nova largura será definida como o mínimo definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="33579-111">If this parameter is less than the system-defined minimum width, the new width is set to the system-defined minimum.</span></span>

</dd> <dt>

<span data-ttu-id="33579-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33579-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="33579-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="33579-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33579-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33579-114">Return value</span></span>

<span data-ttu-id="33579-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="33579-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33579-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="33579-116">Remarks</span></span>

<span data-ttu-id="33579-117">O valor de recuo mínimo definido pelo sistema normalmente é de cinco pixels, mas não é fixo.</span><span class="sxs-lookup"><span data-stu-id="33579-117">The system-defined minimum indent value is typically five pixels, but it is not fixed.</span></span> <span data-ttu-id="33579-118">Para recuperar o valor exato do recuo mínimo em um sistema específico, envie uma mensagem **TVM \_ SetIndent** com *wParam* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="33579-118">To retrieve the exact value of the minimum indent on a particular system, send a **TVM\_SETINDENT** message with *wParam* set to zero.</span></span> <span data-ttu-id="33579-119">Em seguida, envie uma mensagem [**TVM \_ GetIndent**](tvm-getindent.md) para recuperar o valor mínimo de recuo.</span><span class="sxs-lookup"><span data-stu-id="33579-119">Then send a [**TVM\_GETINDENT**](tvm-getindent.md) message to retrieve the minimum indent value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33579-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33579-120">Requirements</span></span>



| <span data-ttu-id="33579-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="33579-121">Requirement</span></span> | <span data-ttu-id="33579-122">Valor</span><span class="sxs-lookup"><span data-stu-id="33579-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33579-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33579-123">Minimum supported client</span></span><br/> | <span data-ttu-id="33579-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33579-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="33579-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33579-125">Minimum supported server</span></span><br/> | <span data-ttu-id="33579-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33579-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33579-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33579-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="33579-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="33579-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33579-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="33579-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33579-130">**Defaultindent de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="33579-130">**TreeView\_SetIndent**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





