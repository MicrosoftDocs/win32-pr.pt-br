---
title: Mensagem de TVM_SETITEM (commctrl. h)
description: A \_ mensagem TVM SETITEM define alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetItem.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Controles de TVM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455224"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="c3b99-105">\_Mensagem TVM SETITEM</span><span class="sxs-lookup"><span data-stu-id="c3b99-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="c3b99-106">A mensagem **TVM \_ SETITEM** define alguns ou todos os atributos de um item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="c3b99-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="c3b99-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="c3b99-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3b99-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3b99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3b99-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3b99-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3b99-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c3b99-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3b99-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3b99-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3b99-112">Ponteiro para uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém os novos atributos de item.</span><span class="sxs-lookup"><span data-stu-id="c3b99-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="c3b99-113">Com a [versão 4,71](common-control-versions.md) e posterior, você pode usar uma estrutura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c3b99-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3b99-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3b99-114">Return value</span></span>

<span data-ttu-id="c3b99-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c3b99-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3b99-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3b99-116">Remarks</span></span>

<span data-ttu-id="c3b99-117">O membro **hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica o item, e o membro **Mask** especifica quais atributos definir.</span><span class="sxs-lookup"><span data-stu-id="c3b99-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b99-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3b99-118">Requirements</span></span>



| <span data-ttu-id="c3b99-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3b99-119">Requirement</span></span> | <span data-ttu-id="c3b99-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c3b99-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b99-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3b99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3b99-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3b99-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3b99-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3b99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3b99-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3b99-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3b99-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3b99-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3b99-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3b99-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c3b99-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c3b99-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c3b99-128">**TVM \_ SETITEMW** (Unicode) e **TVM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c3b99-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





