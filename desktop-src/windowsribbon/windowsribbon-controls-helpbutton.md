---
title: Botão ajuda
description: O botão ajuda é um controle que o usuário pode clicar para exibir o sistema de ajuda do aplicativo.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917322"
---
# <a name="help-button"></a><span data-ttu-id="9912e-103">Botão ajuda</span><span class="sxs-lookup"><span data-stu-id="9912e-103">Help Button</span></span>

<span data-ttu-id="9912e-104">O botão ajuda é um controle que o usuário pode clicar para exibir o sistema de ajuda do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9912e-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="9912e-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9912e-105">Details</span></span>](#details)
-   [<span data-ttu-id="9912e-106">Propriedades do botão de ajuda</span><span class="sxs-lookup"><span data-stu-id="9912e-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="9912e-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9912e-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="9912e-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9912e-108">Details</span></span>

<span data-ttu-id="9912e-109">A captura de tela a seguir ilustra o botão de ajuda da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="9912e-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![captura de tela mostrando o botão ajuda.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="9912e-111">Propriedades do botão de ajuda</span><span class="sxs-lookup"><span data-stu-id="9912e-111">Help Button Properties</span></span>

<span data-ttu-id="9912e-112">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle do botão de ajuda.</span><span class="sxs-lookup"><span data-stu-id="9912e-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="9912e-113">Normalmente, uma propriedade do botão ajuda é atualizada na interface do usuário da faixa de guia invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="9912e-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="9912e-114">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="9912e-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="9912e-115">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="9912e-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="9912e-116">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="9912e-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="9912e-117">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="9912e-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="9912e-118">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle do botão de ajuda.</span><span class="sxs-lookup"><span data-stu-id="9912e-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="9912e-119">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="9912e-119">Property Key</span></span>                                                                                     | <span data-ttu-id="9912e-120">Observações</span><span class="sxs-lookup"><span data-stu-id="9912e-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="9912e-121">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="9912e-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="9912e-122">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="9912e-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="9912e-123">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="9912e-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="9912e-124">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="9912e-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="9912e-125">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="9912e-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="9912e-126">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="9912e-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="9912e-127">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="9912e-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="9912e-128">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="9912e-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9912e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9912e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9912e-130">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="9912e-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="9912e-131">**Elemento HelpButton**</span><span class="sxs-lookup"><span data-stu-id="9912e-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 