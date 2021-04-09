---
title: Mensagem de TVM_SORTCHILDREN (commctrl. h)
description: Classifica os itens filho do item pai especificado em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SortChildren.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Controles de TVM_SORTCHILDREN de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009701"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="e9ba6-105">\_Mensagem TVM SORTCHILDREN</span><span class="sxs-lookup"><span data-stu-id="e9ba6-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="e9ba6-106">Classifica os itens filho do item pai especificado em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="e9ba6-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .</span><span class="sxs-lookup"><span data-stu-id="e9ba6-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9ba6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9ba6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ba6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9ba6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ba6-110">Valor que especifica se a classificação é recursiva.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="e9ba6-111">Defina *wParam* como **true** para classificar todos os níveis de itens filho abaixo do item pai.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="e9ba6-112">Caso contrário, somente os filhos imediatos do pai serão classificados.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="e9ba6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9ba6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ba6-114">Identificador para o item pai cujos itens filho devem ser classificados.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ba6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9ba6-115">Return value</span></span>

<span data-ttu-id="e9ba6-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9ba6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9ba6-117">Remarks</span></span>

<span data-ttu-id="e9ba6-118">Esta mensagem alphabetizes os itens de árvore usando [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) no nome do item.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="e9ba6-119">Você pode usar a mensagem [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) para personalizar o comportamento de ordenação.</span><span class="sxs-lookup"><span data-stu-id="e9ba6-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ba6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ba6-120">Requirements</span></span>



| <span data-ttu-id="e9ba6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ba6-121">Requirement</span></span> | <span data-ttu-id="e9ba6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ba6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ba6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ba6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ba6-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9ba6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9ba6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ba6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ba6-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9ba6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9ba6-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9ba6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ba6-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ba6-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

