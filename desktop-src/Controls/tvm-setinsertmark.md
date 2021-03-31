---
title: Mensagem de TVM_SETINSERTMARK (commctrl. h)
description: Define a marca de inserção em um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetInsertMark.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Controles de TVM_SETINSERTMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824512"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="e7ee1-105">\_Mensagem TVM SETINSERTMARK</span><span class="sxs-lookup"><span data-stu-id="e7ee1-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="e7ee1-106">Define a marca de inserção em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="e7ee1-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .</span><span class="sxs-lookup"><span data-stu-id="e7ee1-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7ee1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7ee1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ee1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7ee1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ee1-110">Valor **bool** que especifica se a marca de inserção é colocada antes ou depois do item especificado.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="e7ee1-111">Se esse argumento for diferente de zero, a marca de inserção será colocada após o item.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="e7ee1-112">Se esse argumento for zero, a marca de inserção será colocada antes do item.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="e7ee1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7ee1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ee1-114">**HTREEITEM** que especifica em qual item a marca de inserção será colocada.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="e7ee1-115">Se esse argumento for **nulo**, a marca de inserção será removida.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ee1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7ee1-116">Return value</span></span>

<span data-ttu-id="e7ee1-117">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ee1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7ee1-118">Remarks</span></span>

<span data-ttu-id="e7ee1-119">Em algumas circunstâncias, a marca de inserção pode aparecer em dois locais depois que um nó é expandido.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="e7ee1-120">Se você estiver usando marcas de inserção, é recomendável forçar uma atualização do controle depois de expandir um nó.</span><span class="sxs-lookup"><span data-stu-id="e7ee1-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ee1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ee1-121">Requirements</span></span>



| <span data-ttu-id="e7ee1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ee1-122">Requirement</span></span> | <span data-ttu-id="e7ee1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e7ee1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ee1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7ee1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ee1-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7ee1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7ee1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7ee1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ee1-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7ee1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7ee1-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7ee1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ee1-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ee1-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





