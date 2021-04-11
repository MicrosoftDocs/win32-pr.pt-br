---
title: Elemento LISTBOX
description: Elemento LISTBOX
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Capas do Windows Media Player, elemento LISTBOX
- elemento LISTBOX e skins
- Elemento LISTBOX
- referência para capas, elemento LISTBOX
- elementos, LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005305"
---
# <a name="listbox-element"></a><span data-ttu-id="67063-108">Elemento LISTBOX</span><span class="sxs-lookup"><span data-stu-id="67063-108">LISTBOX Element</span></span>

<span data-ttu-id="67063-109">O elemento **ListBox** fornece uma maneira para os usuários selecionarem itens de uma lista.</span><span class="sxs-lookup"><span data-stu-id="67063-109">The **LISTBOX** element provides a way for users to select items from a list.</span></span> <span data-ttu-id="67063-110">Esses itens podem ser especificados usando elementos de **Item** como filhos do elemento **ListBox** .</span><span class="sxs-lookup"><span data-stu-id="67063-110">These items can be specified by using **ITEM** elements as children of the **LISTBOX** element.</span></span> <span data-ttu-id="67063-111">Se você precisar de um controle de caixa de listagem que seja exibido somente quando necessário, use o elemento **Popup** , que é idêntico ao elemento **ListBox** , exceto pelo valor padrão do atributo **Popup** , que determina seu comportamento de exibição.</span><span class="sxs-lookup"><span data-stu-id="67063-111">If you need a list box control that is displayed only when needed, use the **POPUP** element, which is identical to the **LISTBOX** element except for the default value of the **popUp** attribute, which dictates its display behavior.</span></span>

<span data-ttu-id="67063-112">O elemento **ListBox** dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="67063-112">The **LISTBOX** element supports the following attributes.</span></span>



| <span data-ttu-id="67063-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="67063-113">Attribute</span></span>                                        | <span data-ttu-id="67063-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="67063-114">Description</span></span>                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67063-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="67063-115">backgroundColor</span></span>](listbox-backgroundcolor.md)   | <span data-ttu-id="67063-116">Especifica ou recupera a cor do plano de fundo no controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-116">Specifies or retrieves the background color in the list box control.</span></span>                                                  |
| [<span data-ttu-id="67063-117">borda</span><span class="sxs-lookup"><span data-stu-id="67063-117">border</span></span>](listbox-border.md)                     | <span data-ttu-id="67063-118">Especifica ou recupera um valor que indica se o controle da caixa de listagem tem uma borda.</span><span class="sxs-lookup"><span data-stu-id="67063-118">Specifies or retrieves a value indicating whether the list box control has a border.</span></span> <span data-ttu-id="67063-119">Só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="67063-119">Can only be set at design time.</span></span>  |
| [<span data-ttu-id="67063-120">firstVisibleItem</span><span class="sxs-lookup"><span data-stu-id="67063-120">firstVisibleItem</span></span>](listbox-firstvisibleitem.md) | <span data-ttu-id="67063-121">Especifica ou recupera o índice da primeira linha visível no controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-121">Specifies or retrieves the index of the first visible line in the list box control.</span></span>                                   |
| [<span data-ttu-id="67063-122">focusItem</span><span class="sxs-lookup"><span data-stu-id="67063-122">focusItem</span></span>](listbox-focusitem.md)               | <span data-ttu-id="67063-123">Especifica ou recupera a linha que contém o foco.</span><span class="sxs-lookup"><span data-stu-id="67063-123">Specifies or retrieves the line that contains focus.</span></span>                                                                  |
| [<span data-ttu-id="67063-124">fontFace</span><span class="sxs-lookup"><span data-stu-id="67063-124">fontFace</span></span>](listbox-fontface.md)                 | <span data-ttu-id="67063-125">Especifica ou recupera a fonte do controle de caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-125">Specifies or retrieves the font for the list box control.</span></span>                                                             |
| [<span data-ttu-id="67063-126">fontSize</span><span class="sxs-lookup"><span data-stu-id="67063-126">fontSize</span></span>](listbox-fontsize.md)                 | <span data-ttu-id="67063-127">Especifica ou recupera o tamanho da fonte para o controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-127">Specifies or retrieves the font size for the list box control.</span></span>                                                        |
| [<span data-ttu-id="67063-128">fontStyle</span><span class="sxs-lookup"><span data-stu-id="67063-128">fontStyle</span></span>](listbox-fontstyle.md)               | <span data-ttu-id="67063-129">Especifica ou recupera o estilo da fonte para o controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-129">Specifies or retrieves the font style for the list box control.</span></span>                                                       |
| [<span data-ttu-id="67063-130">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="67063-130">foregroundColor</span></span>](listbox-foregroundcolor.md)   | <span data-ttu-id="67063-131">Especifica ou recupera a cor do texto no controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-131">Specifies or retrieves the text color in the list box control.</span></span>                                                        |
| [<span data-ttu-id="67063-132">itemCount</span><span class="sxs-lookup"><span data-stu-id="67063-132">itemCount</span></span>](listbox-itemcount.md)               | <span data-ttu-id="67063-133">Recupera o número de itens no controle caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-133">Retrieves the number of items in the list box control.</span></span>                                                                |
| [<span data-ttu-id="67063-134">Seleção múltipla</span><span class="sxs-lookup"><span data-stu-id="67063-134">multiSelect</span></span>](listbox-multiselect.md)           | <span data-ttu-id="67063-135">Especifica ou recupera um valor que indica se o usuário pode selecionar várias linhas.</span><span class="sxs-lookup"><span data-stu-id="67063-135">Specifies or retrieves a value indicating whether the user can select multiple lines.</span></span> <span data-ttu-id="67063-136">Só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="67063-136">Can only be set at design time.</span></span> |
| [<span data-ttu-id="67063-137">Pop-up</span><span class="sxs-lookup"><span data-stu-id="67063-137">popUp</span></span>](listbox-popup.md)                       | <span data-ttu-id="67063-138">Especifica um valor que indica se o elemento representa um controle de caixa de listagem ou pop-up.</span><span class="sxs-lookup"><span data-stu-id="67063-138">Specifies a value indicating whether the element represents a popup or list box control.</span></span>                              |
| [<span data-ttu-id="67063-139">readOnly</span><span class="sxs-lookup"><span data-stu-id="67063-139">readOnly</span></span>](listbox-readonly.md)                 | <span data-ttu-id="67063-140">Especifica ou recupera um valor que indica se o texto é somente leitura ou se o texto pode ser selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="67063-140">Specifies or retrieves a value indicating whether text is read-only or text can be selected by the user.</span></span>              |
| [<span data-ttu-id="67063-141">selectedItem</span><span class="sxs-lookup"><span data-stu-id="67063-141">selectedItem</span></span>](listbox-selecteditem.md)         | <span data-ttu-id="67063-142">Especifica ou recupera o índice do item selecionado no controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-142">Specifies or retrieves the index of the item selected in the list box control.</span></span>                                        |
| [<span data-ttu-id="67063-143">organizados</span><span class="sxs-lookup"><span data-stu-id="67063-143">sorted</span></span>](listbox-sorted.md)                     | <span data-ttu-id="67063-144">Especifica ou recupera um valor que indica se o controle da caixa de listagem está classificado em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="67063-144">Specifies or retrieves a value indicating whether the list box control is sorted alphabetically.</span></span>                      |



 

<span data-ttu-id="67063-145">O elemento **ListBox** dá suporte aos seguintes métodos.</span><span class="sxs-lookup"><span data-stu-id="67063-145">The **LISTBOX** element supports the following methods.</span></span>



| <span data-ttu-id="67063-146">Método</span><span class="sxs-lookup"><span data-stu-id="67063-146">Method</span></span>                                                 | <span data-ttu-id="67063-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="67063-147">Description</span></span>                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67063-148">appendItem</span><span class="sxs-lookup"><span data-stu-id="67063-148">appendItem</span></span>](listbox-appenditem.md)                   | <span data-ttu-id="67063-149">Insere um novo texto no final do controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-149">Inserts new text at the end of the list box control.</span></span>                                                                  |
| [<span data-ttu-id="67063-150">deleteAll</span><span class="sxs-lookup"><span data-stu-id="67063-150">deleteAll</span></span>](listbox-deleteall.md)                     | <span data-ttu-id="67063-151">Exclui todos os itens do controle caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-151">Deletes all items from the list box control.</span></span>                                                                          |
| [<span data-ttu-id="67063-152">deleteItem</span><span class="sxs-lookup"><span data-stu-id="67063-152">deleteItem</span></span>](listbox-deleteitem.md)                   | <span data-ttu-id="67063-153">Exclui o item de controle de caixa de listagem no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="67063-153">Deletes the list box control item at the specified index.</span></span>                                                             |
| [<span data-ttu-id="67063-154">desativar</span><span class="sxs-lookup"><span data-stu-id="67063-154">dismiss</span></span>](listbox-dismiss.md)                         | <span data-ttu-id="67063-155">Oculta o controle.</span><span class="sxs-lookup"><span data-stu-id="67063-155">Hides the control.</span></span>                                                                                                    |
| [<span data-ttu-id="67063-156">findItem</span><span class="sxs-lookup"><span data-stu-id="67063-156">findItem</span></span>](listbox-finditem.md)                       | <span data-ttu-id="67063-157">Pesquisa uma determinada cadeia de caracteres começando com o item após o índice de item especificado.</span><span class="sxs-lookup"><span data-stu-id="67063-157">Searches for a given string starting with the item following the specified item index.</span></span>                                |
| [<span data-ttu-id="67063-158">getItem</span><span class="sxs-lookup"><span data-stu-id="67063-158">getItem</span></span>](listbox-getitem.md)                         | <span data-ttu-id="67063-159">Recupera o texto do item com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="67063-159">Retrieves the text for the item with the specified index.</span></span>                                                             |
| [<span data-ttu-id="67063-160">getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="67063-160">getNextSelectedItem</span></span>](listbox-getnextselecteditem.md) | <span data-ttu-id="67063-161">Recupera o próximo item selecionado no controle caixa de listagem, começando no item após aquele com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="67063-161">Retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span> |
| [<span data-ttu-id="67063-162">insertItem</span><span class="sxs-lookup"><span data-stu-id="67063-162">insertItem</span></span>](listbox-insertitem.md)                   | <span data-ttu-id="67063-163">Insere o texto especificado no índice especificado no controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="67063-163">Inserts the specified text at the specified index in the list box control.</span></span>                                            |
| [<span data-ttu-id="67063-164">replaceItem</span><span class="sxs-lookup"><span data-stu-id="67063-164">replaceItem</span></span>](listbox-replaceitem.md)                 | <span data-ttu-id="67063-165">Substitui o texto no índice especificado pelo texto especificado.</span><span class="sxs-lookup"><span data-stu-id="67063-165">Replaces the text at the specified index with the specified text.</span></span>                                                     |
| [<span data-ttu-id="67063-166">setselecionostate</span><span class="sxs-lookup"><span data-stu-id="67063-166">setSelectedState</span></span>](listbox-setselectedstate.md)       | <span data-ttu-id="67063-167">Seleciona ou anula a seleção do item com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="67063-167">Selects or unselects the item with the specified index.</span></span>                                                               |
| [<span data-ttu-id="67063-168">show</span><span class="sxs-lookup"><span data-stu-id="67063-168">show</span></span>](listbox-show.md)                               | <span data-ttu-id="67063-169">Exibe o controle.</span><span class="sxs-lookup"><span data-stu-id="67063-169">Displays the control.</span></span>                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="67063-170">Esse elemento requer o Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="67063-170">This element requires Windows Media Player for Windows XP or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="67063-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67063-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67063-172">**Elemento POPUP**</span><span class="sxs-lookup"><span data-stu-id="67063-172">**POPUP Element**</span></span>](popup-element.md)
</dt> <dt>

[<span data-ttu-id="67063-173">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="67063-173">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




