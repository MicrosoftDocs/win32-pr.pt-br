---
title: Galeria de Drop-Down
description: A Galeria de Drop-Down consiste em um botão que, quando clicado, exibe uma lista suspensa contendo uma coleção de itens ou comandos mutuamente exclusivos.
ms.assetid: 10644e10-f903-49f6-aecd-1a63d97fe447
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07553dcc767b50786e271544ea44bd17670a2a9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642326"
---
# <a name="drop-down-gallery"></a><span data-ttu-id="95c84-103">Galeria de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="95c84-103">Drop-Down Gallery</span></span>

<span data-ttu-id="95c84-104">A Galeria de Drop-Down consiste em um botão que, quando clicado, exibe uma lista suspensa contendo uma coleção de itens ou comandos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="95c84-104">The Drop-Down Gallery consists of a button that when clicked displays a drop-down list containing a collection of mutually exclusive items or Commands.</span></span>

-   [<span data-ttu-id="95c84-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="95c84-105">Details</span></span>](#details)
-   [<span data-ttu-id="95c84-106">Propriedades da Galeria suspensa</span><span class="sxs-lookup"><span data-stu-id="95c84-106">Drop-Down Gallery Properties</span></span>](#drop-down-gallery-properties)
-   [<span data-ttu-id="95c84-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95c84-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="95c84-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="95c84-108">Details</span></span>

<span data-ttu-id="95c84-109">Esse controle é útil para expor itens relacionados ou comandos em que não há nenhum padrão óbvio, e os itens individuais podem ser representados por uma imagem, texto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="95c84-109">This control is useful for exposing related items or Commands where there is no obvious default, and the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="95c84-110">O suporte para barras de garra vertical e de canto, ou identificadores de redimensionamento, é fornecido por meio do elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="95c84-110">Support for both vertical and corner gripper bars, or resizing handles, is provided through the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) element.</span></span>

<span data-ttu-id="95c84-111">A captura de tela a seguir ilustra a Galeria de Drop-Down da faixa de opções no Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="95c84-111">The following screen shot illustrates the Ribbon Drop-Down Gallery in Microsoft Paint.</span></span>

![captura de tela de um controle dropdowngallery na faixa de faixas do Microsoft Paint.](images/controls/dropdowngallery.png)

## <a name="drop-down-gallery-properties"></a><span data-ttu-id="95c84-113">Propriedades da Galeria de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="95c84-113">Drop-Down Gallery Properties</span></span>

<span data-ttu-id="95c84-114">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle da galeria de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="95c84-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Gallery control.</span></span>

<span data-ttu-id="95c84-115">Normalmente, uma propriedade de galeria de Drop-Down é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="95c84-115">Typically, a Drop-Down Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="95c84-116">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="95c84-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="95c84-117">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="95c84-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="95c84-118">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="95c84-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="95c84-119">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="95c84-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="95c84-120">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle da Galeria de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="95c84-120">The following table lists the property keys that are associated with the Drop-Down Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95c84-121">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="95c84-121">Property Key</span></span></th>
<th><span data-ttu-id="95c84-122">Observações</span><span class="sxs-lookup"><span data-stu-id="95c84-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95c84-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="95c84-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="95c84-124">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="95c84-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c84-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="95c84-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="95c84-126">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="95c84-126">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95c84-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="95c84-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="95c84-128">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="95c84-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c84-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="95c84-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="95c84-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95c84-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="95c84-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="95c84-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c84-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="95c84-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="95c84-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95c84-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="95c84-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="95c84-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c84-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(válido somente para uma galeria de itens)</span><span class="sxs-lookup"><span data-stu-id="95c84-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="95c84-138">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="95c84-138">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="95c84-139">Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.</span><span class="sxs-lookup"><span data-stu-id="95c84-139">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95c84-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="95c84-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="95c84-141">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c84-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="95c84-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="95c84-143">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95c84-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="95c84-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="95c84-145">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95c84-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="95c84-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="95c84-147">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="95c84-147">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="95c84-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95c84-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95c84-149">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="95c84-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="95c84-150">**Elemento de marcação DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="95c84-150">**DropDownGallery markup element**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="95c84-151">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="95c84-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="95c84-152">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="95c84-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

