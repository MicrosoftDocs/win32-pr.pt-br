---
title: Grupo de guias
description: Um grupo de guias é um controle contextual que é oculto ou exibido em tempo de execução, com base em um documento ou em um estado de espaço de trabalho. O grupo de guias contém um conjunto de controles de guia relacionados ao contexto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294351"
---
# <a name="tab-group"></a><span data-ttu-id="7e881-104">Grupo de guias</span><span class="sxs-lookup"><span data-stu-id="7e881-104">Tab Group</span></span>

<span data-ttu-id="7e881-105">Um grupo de guias é um controle contextual que é oculto ou exibido em tempo de execução, com base em um documento ou em um estado de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7e881-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="7e881-106">O grupo de guias contém um conjunto de controles de [guia](windowsribbon-controls-tab.md) relacionados ao contexto.</span><span class="sxs-lookup"><span data-stu-id="7e881-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="7e881-107">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7e881-107">Details</span></span>](#details)
-   [<span data-ttu-id="7e881-108">Propriedades do grupo de guias</span><span class="sxs-lookup"><span data-stu-id="7e881-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="7e881-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e881-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="7e881-110">Detalhes</span><span class="sxs-lookup"><span data-stu-id="7e881-110">Details</span></span>

<span data-ttu-id="7e881-111">Normalmente, um grupo de guias é exibido durante os Estados específicos do documento ou do espaço de trabalho, como quando um usuário seleciona um determinado tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="7e881-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="7e881-112">Por exemplo, a seleção de uma imagem contida no cabeçalho de uma tabela pode exigir que várias guias contextuais sejam exibidas, expondo a funcionalidade de tabela e imagem.</span><span class="sxs-lookup"><span data-stu-id="7e881-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e881-113">Um grupo de guias não dá suporte A [modos de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="7e881-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="7e881-114">No entanto, os controles de [guia](windowsribbon-controls-tab.md) individuais dentro de um grupo de guias podem.</span><span class="sxs-lookup"><span data-stu-id="7e881-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="7e881-115">A captura de tela a seguir mostra uma [guia](windowsribbon-controls-tab.md) contextual do Paint do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7e881-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![captura de tela que mostra um controle de guia contextual.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="7e881-117">Propriedades do grupo de guias</span><span class="sxs-lookup"><span data-stu-id="7e881-117">Tab Group Properties</span></span>

<span data-ttu-id="7e881-118">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de grupo de guias.</span><span class="sxs-lookup"><span data-stu-id="7e881-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="7e881-119">Normalmente, uma propriedade de grupo de guias é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="7e881-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="7e881-120">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="7e881-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="7e881-121">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="7e881-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="7e881-122">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="7e881-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="7e881-123">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="7e881-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="7e881-124">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de grupo de guias.</span><span class="sxs-lookup"><span data-stu-id="7e881-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="7e881-125">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="7e881-125">Property Key</span></span>                                                                                     | <span data-ttu-id="7e881-126">Observações</span><span class="sxs-lookup"><span data-stu-id="7e881-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e881-127">\_ContextAvailable PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="7e881-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="7e881-128">Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="7e881-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="7e881-129">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="7e881-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="7e881-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="7e881-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7e881-131">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="7e881-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="7e881-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="7e881-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7e881-133">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="7e881-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="7e881-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="7e881-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7e881-135">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="7e881-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="7e881-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="7e881-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="7e881-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e881-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e881-138">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="7e881-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="7e881-139">**Elemento de marcação TabGroup**</span><span class="sxs-lookup"><span data-stu-id="7e881-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 