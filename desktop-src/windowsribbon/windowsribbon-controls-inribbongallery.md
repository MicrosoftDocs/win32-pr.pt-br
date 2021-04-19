---
title: Galeria de In-Ribbon
description: A Galeria de In-Ribbon é um controle que exibe uma coleção de itens ou comandos relacionados na faixa de faixas. Se houver muitos itens na Galeria, será fornecida uma seta de expansão para exibir o restante da coleção em um painel expandido.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef644128204fa0b20284dbb63368ef530b0dd0b3
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105810186"
---
# <a name="in-ribbon-gallery"></a><span data-ttu-id="2e6f5-104">Galeria de In-Ribbon</span><span class="sxs-lookup"><span data-stu-id="2e6f5-104">In-Ribbon Gallery</span></span>

<span data-ttu-id="2e6f5-105">A Galeria de In-Ribbon é um controle que exibe uma coleção de itens ou comandos relacionados na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-105">The In-Ribbon Gallery is a control that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="2e6f5-106">Se houver muitos itens na Galeria, será fornecida uma seta de expansão para exibir o restante da coleção em um painel expandido.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-106">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

-   [<span data-ttu-id="2e6f5-107">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2e6f5-107">Details</span></span>](#details)
-   [<span data-ttu-id="2e6f5-108">Propriedades da galeria na faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="2e6f5-108">In-Ribbon Gallery Properties</span></span>](#in-ribbon-gallery-properties)
-   [<span data-ttu-id="2e6f5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e6f5-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="2e6f5-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2e6f5-110">Details</span></span>

<span data-ttu-id="2e6f5-111">A captura de tela a seguir ilustra o controle da Galeria de In-Ribbon da faixa de opções no Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-111">The following screen shot illustrates the Ribbon In-Ribbon Gallery control in Microsoft Paint.</span></span>

![captura de tela de um controle inribbongallery na faixa de faixas do Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a><span data-ttu-id="2e6f5-113">Propriedades da Galeria de In-Ribbon</span><span class="sxs-lookup"><span data-stu-id="2e6f5-113">In-Ribbon Gallery Properties</span></span>

<span data-ttu-id="2e6f5-114">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle da galeria de In-Ribbon.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the In-Ribbon Gallery control.</span></span>

<span data-ttu-id="2e6f5-115">Normalmente, uma propriedade de galeria de In-Ribbon é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="2e6f5-115">Typically, an In-Ribbon Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2e6f5-116">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="2e6f5-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2e6f5-117">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2e6f5-118">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2e6f5-119">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="2e6f5-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2e6f5-120">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle da Galeria de In-Ribbon.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-120">The following table lists the property keys that are associated with the In-Ribbon Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2e6f5-121">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="2e6f5-121">Property Key</span></span></th>
<th><span data-ttu-id="2e6f5-122">Observações</span><span class="sxs-lookup"><span data-stu-id="2e6f5-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e6f5-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="2e6f5-124">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6f5-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="2e6f5-126">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-126">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6f5-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="2e6f5-128">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6f5-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="2e6f5-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6f5-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="2e6f5-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6f5-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2e6f5-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6f5-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="2e6f5-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6f5-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(válido somente para uma galeria de itens)</span><span class="sxs-lookup"><span data-stu-id="2e6f5-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="2e6f5-138">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-138">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2e6f5-139">Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-139">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6f5-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2e6f5-141">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6f5-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="2e6f5-143">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6f5-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="2e6f5-145">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6f5-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="2e6f5-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="2e6f5-147">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2e6f5-147">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2e6f5-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e6f5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e6f5-149">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="2e6f5-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2e6f5-150">**Elemento InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="2e6f5-150">**InRibbonGallery element**</span></span>](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="2e6f5-151">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="2e6f5-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="2e6f5-152">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="2e6f5-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

