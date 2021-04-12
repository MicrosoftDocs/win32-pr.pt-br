---
title: Mensagem de TVM_DELETEITEM (commctrl. h)
description: Remove um item e todos os seus filhos de um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Controles de TVM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455225"
---
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="2c069-105">\_Mensagem TVM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="2c069-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="2c069-106">Remove um item e todos os seus filhos de um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="2c069-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="2c069-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="2c069-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c069-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c069-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c069-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2c069-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2c069-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2c069-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c069-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c069-112">**HTREEITEM** o identificador para o item a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2c069-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="2c069-113">Se *lParam* for definido como TVI \_ root ou como **NULL**, todos os itens serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="2c069-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="2c069-114">Você também pode usar a macro [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) para excluir todos os itens.</span><span class="sxs-lookup"><span data-stu-id="2c069-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c069-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c069-115">Return value</span></span>

<span data-ttu-id="2c069-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2c069-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c069-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c069-117">Remarks</span></span>

<span data-ttu-id="2c069-118">Não é seguro excluir itens em resposta a uma notificação como [TVN \_ SELCHANGING](tvn-selchanging.md).</span><span class="sxs-lookup"><span data-stu-id="2c069-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="2c069-119">Depois que um item é excluído, seu identificador é inválido e não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="2c069-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="2c069-120">A janela pai recebe um código de notificação [TVN \_ DELETEITEM](tvn-deleteitem.md) quando cada item é removido.</span><span class="sxs-lookup"><span data-stu-id="2c069-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="2c069-121">Se o rótulo do item estiver sendo editado, a operação de edição será cancelada e a janela pai receberá o código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="2c069-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="2c069-122">Se você excluir todos os itens de um controle de exibição de árvore que tem o estilo [**\_ NoScroll de TVs**](tree-view-control-window-styles.md) , os itens adicionados subsequentemente poderão não ser exibidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="2c069-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="2c069-123">Para obter mais informações, consulte [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span><span class="sxs-lookup"><span data-stu-id="2c069-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c069-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c069-124">Requirements</span></span>



| <span data-ttu-id="2c069-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c069-125">Requirement</span></span> | <span data-ttu-id="2c069-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2c069-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c069-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c069-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c069-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c069-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c069-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c069-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c069-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c069-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c069-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c069-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c069-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c069-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





