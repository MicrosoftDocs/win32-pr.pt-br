---
title: Mensagem de TVM_EXPAND (commctrl. h)
description: A \_ mensagem de expansão TVM expande ou recolhe a lista de itens filho associados ao item pai especificado, se houver. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ expansão do TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Controles de TVM_EXPAND de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455736"
---
# <a name="tvm_expand-message"></a><span data-ttu-id="44a28-105">TVM \_ expandir mensagem</span><span class="sxs-lookup"><span data-stu-id="44a28-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="44a28-106">A mensagem de **\_ expansão TVM** expande ou recolhe a lista de itens filho associados ao item pai especificado, se houver.</span><span class="sxs-lookup"><span data-stu-id="44a28-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="44a28-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ expansão do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .</span><span class="sxs-lookup"><span data-stu-id="44a28-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="44a28-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44a28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a28-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44a28-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44a28-110">Sinalizador de ação.</span><span class="sxs-lookup"><span data-stu-id="44a28-110">Action flag.</span></span> <span data-ttu-id="44a28-111">Esse parâmetro pode ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="44a28-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="44a28-112">Valor</span><span class="sxs-lookup"><span data-stu-id="44a28-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="44a28-113">Significado</span><span class="sxs-lookup"><span data-stu-id="44a28-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="44a28-114"><dt>**\_recolher TVE**</dt></span><span class="sxs-lookup"><span data-stu-id="44a28-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="44a28-115">Recolhe a lista.</span><span class="sxs-lookup"><span data-stu-id="44a28-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="44a28-116"><dt>**TVE \_ COLLAPSERESET**</dt></span><span class="sxs-lookup"><span data-stu-id="44a28-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="44a28-117">Recolhe a lista e remove os itens filho.</span><span class="sxs-lookup"><span data-stu-id="44a28-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="44a28-118">O sinalizador de estado [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) é redefinido.</span><span class="sxs-lookup"><span data-stu-id="44a28-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="44a28-119">Esse sinalizador deve ser usado com o \_ sinalizador de recolhimento TVE.</span><span class="sxs-lookup"><span data-stu-id="44a28-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="44a28-120"><dt>**TVE \_ expandir**</dt></span><span class="sxs-lookup"><span data-stu-id="44a28-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="44a28-121">Expande a lista.</span><span class="sxs-lookup"><span data-stu-id="44a28-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="44a28-122"><dt>**TVE \_ EXPANDPARTIAL**</dt></span><span class="sxs-lookup"><span data-stu-id="44a28-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="44a28-123">[Versão 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="44a28-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="44a28-124">Expande parcialmente a lista.</span><span class="sxs-lookup"><span data-stu-id="44a28-124">Partially expands the list.</span></span> <span data-ttu-id="44a28-125">Nesse estado, os itens filho são visíveis e o sinal de adição (+) do item pai, indicando que ele pode ser expandido, é exibido.</span><span class="sxs-lookup"><span data-stu-id="44a28-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="44a28-126">Esse sinalizador deve ser usado em combinação com o \_ sinalizador de expansão TVE.</span><span class="sxs-lookup"><span data-stu-id="44a28-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="44a28-127"><dt>**alternância de TVE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="44a28-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="44a28-128">Recolhe a lista se ela for expandida ou a expandir se ela estiver recolhida.</span><span class="sxs-lookup"><span data-stu-id="44a28-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="44a28-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44a28-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44a28-130">Manipule o item pai para expandir ou recolher.</span><span class="sxs-lookup"><span data-stu-id="44a28-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a28-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44a28-131">Return value</span></span>

<span data-ttu-id="44a28-132">Retornará zero se a operação tiver sido bem-sucedida ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="44a28-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44a28-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="44a28-133">Remarks</span></span>

<span data-ttu-id="44a28-134">Expandir um nó que já está expandido é considerado uma operação bem-sucedida e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retorna um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="44a28-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="44a28-135">O recolhimento de um nó retornará zero se o nó já estiver recolhido; caso contrário, ele retornará diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="44a28-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="44a28-136">A tentativa de expandir ou recolher um nó que não tem filhos é considerada uma falha e **SendMessage** retorna zero.</span><span class="sxs-lookup"><span data-stu-id="44a28-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="44a28-137">Quando um item é expandido pela primeira vez por uma mensagem de **\_ expansão TVM** , a ação gera códigos de notificação de TVN e [TVN \_](tvn-itemexpanded.md) de itens de TVIS e o sinalizador de estado [**\_ EXPANDEDONCE**](tree-view-control-item-states.md) do item é definido. [ \_](tvn-itemexpanding.md)</span><span class="sxs-lookup"><span data-stu-id="44a28-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="44a28-138">Desde que esse sinalizador de estado permaneça definido, as mensagens de **\_ expansão TVM** subsequentes não gerarão \_ notificações de TVN ou de doexpanding TVN \_ .</span><span class="sxs-lookup"><span data-stu-id="44a28-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="44a28-139">Para redefinir o sinalizador de estado **TVIS \_ EXPANDEDONCE** , você deve enviar uma mensagem **TVM \_ Expand** com os \_ sinalizadores TVE Collapse e TVE \_ COLLAPSERESET definidos.</span><span class="sxs-lookup"><span data-stu-id="44a28-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="44a28-140">A tentativa de definir explicitamente **TVIS \_ EXPANDEDONCE** resultará em um comportamento imprevisível.</span><span class="sxs-lookup"><span data-stu-id="44a28-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="44a28-141">A operação de expansão poderá falhar se o proprietário do controle TreeView negar a operação em resposta a uma notificação [de \_ TVN](tvn-itemexpanding.md) .</span><span class="sxs-lookup"><span data-stu-id="44a28-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a28-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a28-142">Requirements</span></span>



| <span data-ttu-id="44a28-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a28-143">Requirement</span></span> | <span data-ttu-id="44a28-144">Valor</span><span class="sxs-lookup"><span data-stu-id="44a28-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44a28-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44a28-145">Minimum supported client</span></span><br/> | <span data-ttu-id="44a28-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44a28-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44a28-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44a28-147">Minimum supported server</span></span><br/> | <span data-ttu-id="44a28-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44a28-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44a28-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44a28-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a28-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44a28-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

