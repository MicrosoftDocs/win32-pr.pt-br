---
title: Guia (Windows Ribbon Framework)
description: Uma guia contém grupos de controles relacionados.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294734"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="c6c78-103">Guia (Windows Ribbon Framework)</span><span class="sxs-lookup"><span data-stu-id="c6c78-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="c6c78-104">Uma guia contém [grupos](windowsribbon-controls-group.md) de controles relacionados.</span><span class="sxs-lookup"><span data-stu-id="c6c78-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="c6c78-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="c6c78-105">Details</span></span>](#details)
-   [<span data-ttu-id="c6c78-106">Guia Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6c78-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="c6c78-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6c78-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="c6c78-108">Detalhes</span><span class="sxs-lookup"><span data-stu-id="c6c78-108">Details</span></span>

<span data-ttu-id="c6c78-109">Há três tipos de guia na estrutura da faixa de tipos.</span><span class="sxs-lookup"><span data-stu-id="c6c78-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="c6c78-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6c78-110">Type</span></span>               | <span data-ttu-id="c6c78-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6c78-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c78-112">**Guia núcleo**</span><span class="sxs-lookup"><span data-stu-id="c6c78-112">**Core tab**</span></span>       | <span data-ttu-id="c6c78-113">Guias principais que organizam as funções padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6c78-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="c6c78-114">**Guia contextual**</span><span class="sxs-lookup"><span data-stu-id="c6c78-114">**Contextual tab**</span></span> | <span data-ttu-id="c6c78-115">Guias que são exibidas durante o documento específico ou Estados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c6c78-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="c6c78-116">Por exemplo, se um usuário selecionar um determinado tipo de objeto, como uma imagem contida no cabeçalho de uma tabela, várias guias contextuais poderão ser exibidas para expor a funcionalidade de tabela e imagem.</span><span class="sxs-lookup"><span data-stu-id="c6c78-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="c6c78-117">**Guia modal**</span><span class="sxs-lookup"><span data-stu-id="c6c78-117">**Modal tab**</span></span>      | <span data-ttu-id="c6c78-118">Guias de núcleo que são exibidas durante um documento específico ou [modo de aplicativo](ribbon-applicationmodes.md)de espaço de trabalho, como Visualizar impressão.</span><span class="sxs-lookup"><span data-stu-id="c6c78-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="c6c78-119">A captura de tela a seguir mostra uma guia principal do Paint do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6c78-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![captura de tela que mostra um controle de guia de núcleo.](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="c6c78-121">Guia Propriedades</span><span class="sxs-lookup"><span data-stu-id="c6c78-121">Tab Properties</span></span>

<span data-ttu-id="c6c78-122">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle guia.</span><span class="sxs-lookup"><span data-stu-id="c6c78-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="c6c78-123">Normalmente, uma Propriedade Tab é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="c6c78-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="c6c78-124">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c6c78-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="c6c78-125">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="c6c78-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="c6c78-126">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="c6c78-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="c6c78-127">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="c6c78-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="c6c78-128">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle guia.</span><span class="sxs-lookup"><span data-stu-id="c6c78-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="c6c78-129">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="c6c78-129">Property Key</span></span>                                                                                     | <span data-ttu-id="c6c78-130">Observações</span><span class="sxs-lookup"><span data-stu-id="c6c78-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="c6c78-131">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="c6c78-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="c6c78-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c6c78-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="c6c78-133">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c6c78-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="c6c78-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c6c78-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="c6c78-135">\_TooltipDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c6c78-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="c6c78-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c6c78-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="c6c78-137">\_TooltipTitle PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="c6c78-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="c6c78-138">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="c6c78-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c6c78-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6c78-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6c78-140">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="c6c78-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="c6c78-141">**Elemento de marcação de guia**</span><span class="sxs-lookup"><span data-stu-id="c6c78-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
