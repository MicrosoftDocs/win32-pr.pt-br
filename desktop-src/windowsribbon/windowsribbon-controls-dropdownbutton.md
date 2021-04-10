---
title: Botão de Drop-Down
description: O botão Drop-Down consiste em um botão que, quando clicado, exibe uma lista suspensa de itens mutuamente exclusivos.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87e6a776dd705fe503e5e93ec601baf6cc2b3cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294558"
---
# <a name="drop-down-button"></a><span data-ttu-id="37f37-103">Botão de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="37f37-103">Drop-Down Button</span></span>

<span data-ttu-id="37f37-104">O botão Drop-Down consiste em um botão que, quando clicado, exibe uma lista suspensa de itens mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="37f37-104">The Drop-Down Button consists of a button that when clicked displays a drop-down list of mutually exclusive items.</span></span>

-   [<span data-ttu-id="37f37-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="37f37-105">Details</span></span>](#details)
-   [<span data-ttu-id="37f37-106">Propriedades do botão suspenso</span><span class="sxs-lookup"><span data-stu-id="37f37-106">Drop-Down Button Properties</span></span>](#drop-down-button-properties)
-   [<span data-ttu-id="37f37-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37f37-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="37f37-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="37f37-108">Details</span></span>

<span data-ttu-id="37f37-109">Esse controle é útil para expor itens bem relacionados em casos em que nenhum padrão óbvio está disponível e onde os itens individuais podem ser representados por uma imagem, texto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="37f37-109">This control is useful for exposing closely related items in cases where no obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="37f37-110">A captura de tela a seguir ilustra o botão de Drop-Down da faixa de opções em uma faixa de opções de exemplo.</span><span class="sxs-lookup"><span data-stu-id="37f37-110">The following screen shot illustrates the Ribbon Drop-Down Button in a sample Ribbon.</span></span>

![captura de tela de um controle DropDownButton em uma faixa de uma amostra.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a><span data-ttu-id="37f37-112">Propriedades do botão de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="37f37-112">Drop-Down Button Properties</span></span>

<span data-ttu-id="37f37-113">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle do botão de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="37f37-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Button control.</span></span>

<span data-ttu-id="37f37-114">Normalmente, uma propriedade de botão Drop-Down é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="37f37-114">Typically, a Drop-Down Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="37f37-115">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="37f37-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="37f37-116">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="37f37-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="37f37-117">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="37f37-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="37f37-118">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="37f37-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="37f37-119">A tabela a seguir lista as chaves de propriedade que estão associadas com o controle de botão de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="37f37-119">The following table lists the property keys that are associated with the Drop-Down Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37f37-120">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="37f37-120">Property Key</span></span></th>
<th><span data-ttu-id="37f37-121">Observações</span><span class="sxs-lookup"><span data-stu-id="37f37-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37f37-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="37f37-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="37f37-123">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37f37-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37f37-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="37f37-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="37f37-125">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37f37-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="37f37-126">Se todos os itens filho estiverem desabilitados, a estrutura definirá <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> como false (0).</span><span class="sxs-lookup"><span data-stu-id="37f37-126">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="37f37-127">Caso contrário, se um ou mais itens filhos estiverem habilitados, UI_PKEY_Enabled será definido como true (-1).</span><span class="sxs-lookup"><span data-stu-id="37f37-127">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="37f37-128">A propriedade <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> para o controle de botão de Drop-Down deve ser invalidada depois que um ou mais itens filho são habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="37f37-128">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Drop-Down Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="37f37-129">Isso garante que a estrutura consulta o valor da propriedade atualizado e atualiza o estado do controle botão de Drop-Down na interface do usuário da faixa de da.</span><span class="sxs-lookup"><span data-stu-id="37f37-129">This ensures that the framework queries the updated property value and refreshes the state of the Drop-Down Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37f37-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="37f37-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="37f37-131">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37f37-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37f37-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="37f37-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="37f37-133">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37f37-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="37f37-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="37f37-135">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37f37-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="37f37-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="37f37-137">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37f37-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="37f37-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="37f37-139">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37f37-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="37f37-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="37f37-141">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="37f37-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="37f37-142">Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.</span><span class="sxs-lookup"><span data-stu-id="37f37-142">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37f37-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="37f37-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="37f37-144">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37f37-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="37f37-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="37f37-146">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37f37-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="37f37-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="37f37-148">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37f37-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="37f37-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="37f37-150">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="37f37-150">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="37f37-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="37f37-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37f37-152">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="37f37-152">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="37f37-153">**Elemento de marcação DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="37f37-153">**DropDownButton markup element**</span></span>](windowsribbon-element-dropdownbutton.md)
</dt> </dl>