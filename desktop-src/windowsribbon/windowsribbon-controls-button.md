---
title: Botão (Windows Ribbon Framework)
description: O botão é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085046"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="c2793-103">Botão (Windows Ribbon Framework)</span><span class="sxs-lookup"><span data-stu-id="c2793-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="c2793-104">O botão é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2793-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="c2793-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="c2793-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="c2793-106">Propriedades do botão</span><span class="sxs-lookup"><span data-stu-id="c2793-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="c2793-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2793-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="c2793-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="c2793-108">Introduction</span></span>

<span data-ttu-id="c2793-109">A captura de tela a seguir contém três exemplos do elemento botão da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="c2793-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![captura de tela dos controles de botão na faixa de em Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="c2793-111">Propriedades do botão</span><span class="sxs-lookup"><span data-stu-id="c2793-111">Button Properties</span></span>

<span data-ttu-id="c2793-112">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de botão.</span><span class="sxs-lookup"><span data-stu-id="c2793-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="c2793-113">Normalmente, uma propriedade Button é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="c2793-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="c2793-114">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c2793-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="c2793-115">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="c2793-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="c2793-116">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="c2793-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="c2793-117">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="c2793-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="c2793-118">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de botão.</span><span class="sxs-lookup"><span data-stu-id="c2793-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="c2793-119">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="c2793-119">Property Key</span></span>                                                                                             | <span data-ttu-id="c2793-120">Observações</span><span class="sxs-lookup"><span data-stu-id="c2793-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2793-121">Interface do usuário \_ PKEY \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="c2793-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="c2793-122">Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="c2793-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="c2793-123">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="c2793-124">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-125">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="c2793-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="c2793-126">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-127">\_LabelDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="c2793-128">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-129">\_LargeHighContrastImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="c2793-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-131">\_LargeImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="c2793-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-133">\_SmallHighContrastImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="c2793-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-135">\_SmallImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="c2793-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-137">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="c2793-138">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="c2793-139">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c2793-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="c2793-140">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c2793-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c2793-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2793-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2793-142">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="c2793-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="c2793-143">**Elemento de marcação de botão**</span><span class="sxs-lookup"><span data-stu-id="c2793-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
