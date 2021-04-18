---
title: Botão de Divisão
description: O botão de divisão é um controle composto com o qual o usuário pode selecionar um valor padrão associado a um botão primário ou selecionar em uma lista de valores mutuamente exclusivos exibidos em uma lista suspensa associada a um botão secundário.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105784991"
---
# <a name="split-button"></a><span data-ttu-id="942c4-103">Botão de Divisão</span><span class="sxs-lookup"><span data-stu-id="942c4-103">Split Button</span></span>

<span data-ttu-id="942c4-104">O botão de divisão é um controle composto com o qual o usuário pode selecionar um valor padrão associado a um botão primário ou selecionar em uma lista de valores mutuamente exclusivos exibidos em uma lista suspensa associada a um botão secundário.</span><span class="sxs-lookup"><span data-stu-id="942c4-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="942c4-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="942c4-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="942c4-106">Propriedades do botão de divisão</span><span class="sxs-lookup"><span data-stu-id="942c4-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="942c4-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="942c4-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="942c4-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="942c4-108">Introduction</span></span>

<span data-ttu-id="942c4-109">Esse controle é útil para expor itens bem relacionados em casos em que um padrão óbvio está disponível e onde os itens individuais podem ser representados por uma imagem, texto ou ambos.</span><span class="sxs-lookup"><span data-stu-id="942c4-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="942c4-110">A captura de tela a seguir ilustra o botão de divisão da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="942c4-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![captura de tela de um controle SplitButton em uma faixa de uma amostra.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="942c4-112">Propriedades do botão de divisão</span><span class="sxs-lookup"><span data-stu-id="942c4-112">Split Button Properties</span></span>

<span data-ttu-id="942c4-113">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle do botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="942c4-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="942c4-114">Normalmente, uma propriedade de botão de divisão é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="942c4-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="942c4-115">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="942c4-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="942c4-116">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="942c4-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="942c4-117">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="942c4-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="942c4-118">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="942c4-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="942c4-119">A tabela a seguir lista as chaves de propriedade que estão associadas com o controle de botão de divisão.</span><span class="sxs-lookup"><span data-stu-id="942c4-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="942c4-120">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="942c4-120">Property Key</span></span></th>
<th><span data-ttu-id="942c4-121">Observações</span><span class="sxs-lookup"><span data-stu-id="942c4-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="942c4-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="942c4-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="942c4-123">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="942c4-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="942c4-124">Se todos os itens filho estiverem desabilitados, a estrutura definirá <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> como false (0).</span><span class="sxs-lookup"><span data-stu-id="942c4-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="942c4-125">Caso contrário, se um ou mais itens filhos estiverem habilitados, UI_PKEY_Enabled será definido como true (-1).</span><span class="sxs-lookup"><span data-stu-id="942c4-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="942c4-126">A propriedade <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> para o controle do botão de divisão deve ser invalidada depois que um ou mais itens filho são habilitados ou desabilitados.</span><span class="sxs-lookup"><span data-stu-id="942c4-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="942c4-127">Isso garante que a estrutura consulta o valor da propriedade atualizado e atualiza o estado do controle do botão de divisão na interface do usuário da faixa de da.</span><span class="sxs-lookup"><span data-stu-id="942c4-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="942c4-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="942c4-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="942c4-129">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="942c4-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="942c4-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="942c4-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="942c4-131">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="942c4-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="942c4-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="942c4-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="942c4-133">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="942c4-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="942c4-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="942c4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="942c4-135">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="942c4-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="942c4-136">**Elemento de marcação SplitButton**</span><span class="sxs-lookup"><span data-stu-id="942c4-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>