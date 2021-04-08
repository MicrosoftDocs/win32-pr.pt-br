---
title: Mensagem de TVM_GETITEM (commctrl. h)
description: Recupera alguns ou todos os atributos de um item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetItem.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Controles de TVM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086520"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="def2d-105">\_Mensagem TVM GETITEM</span><span class="sxs-lookup"><span data-stu-id="def2d-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="def2d-106">Recupera alguns ou todos os atributos de um item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="def2d-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="def2d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .</span><span class="sxs-lookup"><span data-stu-id="def2d-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="def2d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="def2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def2d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="def2d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="def2d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="def2d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="def2d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="def2d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="def2d-112">Ponteiro para uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que especifica as informações para recuperar e receber informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="def2d-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="def2d-113">Com a [versão 4,71](common-control-versions.md) e posterior, você pode usar uma estrutura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="def2d-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def2d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="def2d-114">Return value</span></span>

<span data-ttu-id="def2d-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="def2d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="def2d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="def2d-116">Remarks</span></span>

<span data-ttu-id="def2d-117">Quando a mensagem é enviada, o membro **hItem** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica o item sobre o qual recuperar informações e o membro **Mask** especifica os atributos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="def2d-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="def2d-118">Se o \_ sinalizador de texto TVIF for definido no membro **Mask** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) ou [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , o membro **pszText** deverá apontar para um buffer válido e o membro **cchTextMax** deverá ser definido como o número de caracteres nesse buffer.</span><span class="sxs-lookup"><span data-stu-id="def2d-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="def2d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def2d-119">Requirements</span></span>



| <span data-ttu-id="def2d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="def2d-120">Requirement</span></span> | <span data-ttu-id="def2d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="def2d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="def2d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def2d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="def2d-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="def2d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="def2d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def2d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="def2d-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="def2d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="def2d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="def2d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="def2d-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="def2d-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="def2d-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="def2d-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="def2d-129">**TVM \_ GETITEMW** (Unicode) e **TVM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="def2d-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





