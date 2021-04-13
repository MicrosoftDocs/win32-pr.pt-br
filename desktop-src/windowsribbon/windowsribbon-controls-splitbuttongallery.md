---
title: Galeria de botões de divisão
description: A Galeria de botões de divisão é um controle composto que contém um botão primário que expõe um único item ou comando padrão, e um botão secundário que, quando clicado, exibe o restante do item ou da coleção de comandos em uma lista suspensa mutuamente exclusiva.
ms.assetid: c0fcfe72-d2e9-465d-941a-b3832b36b8c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1865949c1b6f3e274b01d0b4e454dc42e619c2c0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104366810"
---
# <a name="split-button-gallery"></a><span data-ttu-id="23855-103">Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="23855-103">Split Button Gallery</span></span>

<span data-ttu-id="23855-104">A Galeria de botões de divisão é um controle composto que contém um botão primário que expõe um único item ou comando padrão, e um botão secundário que, quando clicado, exibe o restante do item ou da coleção de comandos em uma lista suspensa mutuamente exclusiva.</span><span class="sxs-lookup"><span data-stu-id="23855-104">The Split Button Gallery is a composite control that contains a primary button which exposes a single default item or Command, and a secondary button which when clicked displays the rest of the item or Command collection in a mutually exclusive drop-down list.</span></span>

-   [<span data-ttu-id="23855-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="23855-105">Details</span></span>](#details)
-   [<span data-ttu-id="23855-106">Propriedades da Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="23855-106">Split Button Gallery Properties</span></span>](#split-button-gallery-properties)
-   [<span data-ttu-id="23855-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23855-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="23855-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="23855-108">Details</span></span>

<span data-ttu-id="23855-109">Esse controle é útil para expor itens bem relacionados em casos em que um padrão óbvio está disponível e onde os itens individuais podem ser representados por uma imagem, texto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="23855-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="23855-110">A captura de tela a seguir ilustra a Galeria de botões de divisão da faixa de opções no Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="23855-110">The following screen shot illustrates the Ribbon Split Button Gallery in Microsoft Paint.</span></span>

![captura de tela de um controle splitbuttongallery na faixa de faixas do Microsoft Paint.](images/controls/splitbuttongallery.png)

## <a name="split-button-gallery-properties"></a><span data-ttu-id="23855-112">Propriedades da Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="23855-112">Split Button Gallery Properties</span></span>

<span data-ttu-id="23855-113">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle da Galeria de botões de divisão.</span><span class="sxs-lookup"><span data-stu-id="23855-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button Gallery control.</span></span>

<span data-ttu-id="23855-114">Normalmente, uma propriedade da Galeria de botões de divisão é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="23855-114">Typically, a Split Button Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="23855-115">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="23855-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="23855-116">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="23855-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="23855-117">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="23855-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="23855-118">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="23855-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="23855-119">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle Galeria de botões de divisão.</span><span class="sxs-lookup"><span data-stu-id="23855-119">The following table lists the property keys that are associated with the Split Button Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23855-120">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="23855-120">Property Key</span></span></th>
<th><span data-ttu-id="23855-121">Observações</span><span class="sxs-lookup"><span data-stu-id="23855-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23855-122"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="23855-122"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="23855-123">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="23855-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23855-124"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="23855-124"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="23855-125">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="23855-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23855-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="23855-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="23855-127">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="23855-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23855-128"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="23855-128"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="23855-129">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="23855-129">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23855-130"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="23855-130"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="23855-131">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23855-132"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="23855-132"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="23855-133">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23855-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="23855-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="23855-135">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23855-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="23855-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="23855-137">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23855-138"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(válido somente para uma galeria de itens)</span><span class="sxs-lookup"><span data-stu-id="23855-138"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="23855-139">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="23855-139">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="23855-140">Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.</span><span class="sxs-lookup"><span data-stu-id="23855-140">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23855-141"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="23855-141"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="23855-142">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23855-143"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="23855-143"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="23855-144">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23855-145"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="23855-145"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="23855-146">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="23855-147"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="23855-147"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="23855-148">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="23855-148">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="23855-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23855-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23855-150">**Elemento de marcação SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="23855-150">**SplitButtonGallery markup element**</span></span>](windowsribbon-element-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="23855-151">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="23855-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="23855-152">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="23855-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

