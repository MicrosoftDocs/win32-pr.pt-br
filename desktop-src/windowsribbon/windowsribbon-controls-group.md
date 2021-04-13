---
title: Grupo (Windows Ribbon Framework)
description: O grupo organiza comandos e controles relacionados em uma guia.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369165"
---
# <a name="group-windows-ribbon-framework"></a><span data-ttu-id="2597a-103">Grupo (Windows Ribbon Framework)</span><span class="sxs-lookup"><span data-stu-id="2597a-103">Group (Windows Ribbon Framework)</span></span>

<span data-ttu-id="2597a-104">O grupo organiza comandos e controles relacionados em uma [guia](windowsribbon-controls-tab.md).</span><span class="sxs-lookup"><span data-stu-id="2597a-104">The Group organizes related Commands and controls within a [Tab](windowsribbon-controls-tab.md).</span></span>

-   [<span data-ttu-id="2597a-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2597a-105">Details</span></span>](#details)
-   [<span data-ttu-id="2597a-106">Propriedades do grupo</span><span class="sxs-lookup"><span data-stu-id="2597a-106">Group Properties</span></span>](#group-properties)
-   [<span data-ttu-id="2597a-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2597a-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="2597a-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="2597a-108">Details</span></span>

<span data-ttu-id="2597a-109">A captura de tela a seguir ilustra o controle de grupo da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="2597a-109">The following screen shot illustrates the Ribbon Group control.</span></span>

![captura de tela com textos explicativos mostrando um grupo.](images/controls/group.png)

## <a name="group-properties"></a><span data-ttu-id="2597a-111">Propriedades do grupo</span><span class="sxs-lookup"><span data-stu-id="2597a-111">Group Properties</span></span>

<span data-ttu-id="2597a-112">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de grupo.</span><span class="sxs-lookup"><span data-stu-id="2597a-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Group control.</span></span>

<span data-ttu-id="2597a-113">Normalmente, uma propriedade de grupo é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="2597a-113">Typically, a Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="2597a-114">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="2597a-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="2597a-115">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="2597a-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="2597a-116">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="2597a-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="2597a-117">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="2597a-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="2597a-118">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de grupo.</span><span class="sxs-lookup"><span data-stu-id="2597a-118">The following table lists the property keys that are associated with the Group control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2597a-119">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="2597a-119">Property Key</span></span></th>
<th><span data-ttu-id="2597a-120">Observações</span><span class="sxs-lookup"><span data-stu-id="2597a-120">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2597a-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="2597a-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="2597a-122">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-122">Can only be updated through invalidation.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2597a-123">A estrutura requer que o valor de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> para um controle de grupo comece com a letra maiúscula Z. Se o valor fornecido pelo aplicativo no método de retorno de chamada <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler:: updateproperty</strong></a> não começar com a letra Z, esse valor será ignorado e um valor será gerado pela estrutura em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2597a-123">The framework requires that the value of <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> for a Group control begins with the upper-case letter Z. If the value supplied by the application in the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> callback method does not begin with the letter Z, this value is ignored and a value is generated by the framework instead.</span></span> <span data-ttu-id="2597a-124">O valor da estrutura é a letra Z seguida de um valor numérico começando em 1 e aumentando sequencialmente, conforme necessário, para os controles de grupo subsequentes (Z1, Z2,..., ZX).</span><span class="sxs-lookup"><span data-stu-id="2597a-124">The framework value is the letter Z followed by a numeric value starting at 1 and increasing sequentially, as required, for subsequent Group controls (Z1, Z2, ..., Zx).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2597a-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="2597a-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="2597a-126">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-126">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2597a-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2597a-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2597a-128">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-128">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2597a-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="2597a-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="2597a-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2597a-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="2597a-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="2597a-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2597a-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="2597a-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="2597a-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2597a-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="2597a-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="2597a-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2597a-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="2597a-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="2597a-138">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="2597a-138">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2597a-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2597a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2597a-140">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="2597a-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="2597a-141">**Elemento Group**</span><span class="sxs-lookup"><span data-stu-id="2597a-141">**Group element**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

