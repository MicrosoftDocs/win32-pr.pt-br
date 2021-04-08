---
title: Mensagem de TVM_SELECTITEM (commctrl. h)
description: Seleciona o item de exibição de árvore especificado, rola o item para a exibição ou redesenha o item no estilo usado para indicar o destino de uma operação de arrastar e soltar.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Controles de TVM_SELECTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824244"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="caeec-104">\_Mensagem TVM SELECTITEM</span><span class="sxs-lookup"><span data-stu-id="caeec-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="caeec-105">Seleciona o item de exibição de árvore especificado, rola o item para a exibição ou redesenha o item no estilo usado para indicar o destino de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="caeec-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="caeec-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)ou [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="caeec-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="caeec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caeec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caeec-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="caeec-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caeec-109">Sinalizador de ação.</span><span class="sxs-lookup"><span data-stu-id="caeec-109">Action flag.</span></span> <span data-ttu-id="caeec-110">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="caeec-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="caeec-111">Valor</span><span class="sxs-lookup"><span data-stu-id="caeec-111">Value</span></span></th>
<th><span data-ttu-id="caeec-112">Significado</span><span class="sxs-lookup"><span data-stu-id="caeec-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="caeec-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="caeec-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="caeec-114">Define a seleção para o item especificado.</span><span class="sxs-lookup"><span data-stu-id="caeec-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="caeec-115">A janela pai do controle de exibição de árvore recebe os códigos de notificação <a href="tvn-selchanging.md">TVN_SELCHANGING</a> e <a href="tvn-selchanged.md">TVN_SELCHANGED</a> .</span><span class="sxs-lookup"><span data-stu-id="caeec-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="caeec-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="caeec-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="caeec-117">Redesenha o item especificado no estilo usado para indicar o destino de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="caeec-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="caeec-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="caeec-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="caeec-119">Garante que o item especificado esteja visível e, se possível, exiba-o na parte superior da janela do controle.</span><span class="sxs-lookup"><span data-stu-id="caeec-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="caeec-120">Os controles de exibição de árvore exibem quantos itens forem ajustados na janela.</span><span class="sxs-lookup"><span data-stu-id="caeec-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="caeec-121">Se o item especificado estiver próximo da parte inferior da hierarquia de itens do controle, ele poderá não se tornar o primeiro item visível, dependendo de quantos itens couberem na janela.</span><span class="sxs-lookup"><span data-stu-id="caeec-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="caeec-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="caeec-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="caeec-123">Quando um único item é selecionado, o modo de exibição de árvore não expande os filhos desse item.</span><span class="sxs-lookup"><span data-stu-id="caeec-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="caeec-124">Isso é válido somente se usado com o sinalizador TVGN_CARET.</span><span class="sxs-lookup"><span data-stu-id="caeec-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="caeec-125">Para usar esse sinalizador, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="caeec-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="caeec-126">Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</span><span class="sxs-lookup"><span data-stu-id="caeec-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="caeec-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="caeec-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caeec-128">Identificador para um item.</span><span class="sxs-lookup"><span data-stu-id="caeec-128">Handle to an item.</span></span> <span data-ttu-id="caeec-129">Se *lParam* for **NULL**, o controle será definido como não tem nenhum item selecionado.</span><span class="sxs-lookup"><span data-stu-id="caeec-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caeec-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="caeec-130">Return value</span></span>

<span data-ttu-id="caeec-131">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="caeec-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="caeec-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="caeec-132">Remarks</span></span>

<span data-ttu-id="caeec-133">Se o item especificado for o filho de um item pai recolhido, a lista de itens filho do pai será expandida para revelar o item especificado.</span><span class="sxs-lookup"><span data-stu-id="caeec-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="caeec-134">Nesse caso, a janela pai do controle recebe os códigos de notificação [TVN \_ doexpanding](tvn-itemexpanding.md) e [TVN \_ ](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="caeec-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="caeec-135">Usar a macro [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) é equivalente a enviar a mensagem **TVM \_ SelectItem** com *wParam* definido para o valor de cursor TVGN \_ .</span><span class="sxs-lookup"><span data-stu-id="caeec-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="caeec-136">Usar a macro [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) é equivalente a enviar a mensagem **TVM \_ SELECTITEM** com *wParam* definido para o valor TVGN \_ DROPHILITE.</span><span class="sxs-lookup"><span data-stu-id="caeec-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="caeec-137">Usar [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) é equivalente a enviar a mensagem **TVM \_ SELECTITEM** com *wParam* definido para o \_ valor TVGN FIRSTVISIBLE.</span><span class="sxs-lookup"><span data-stu-id="caeec-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="caeec-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caeec-138">Requirements</span></span>



| <span data-ttu-id="caeec-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="caeec-139">Requirement</span></span> | <span data-ttu-id="caeec-140">Valor</span><span class="sxs-lookup"><span data-stu-id="caeec-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="caeec-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="caeec-141">Minimum supported client</span></span><br/> | <span data-ttu-id="caeec-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="caeec-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="caeec-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="caeec-143">Minimum supported server</span></span><br/> | <span data-ttu-id="caeec-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="caeec-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="caeec-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="caeec-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="caeec-146"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="caeec-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





