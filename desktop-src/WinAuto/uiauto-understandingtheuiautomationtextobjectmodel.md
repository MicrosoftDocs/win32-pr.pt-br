---
title: Compreendendo o modelo de objeto de texto de automação da interface do usuário
description: Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft acessam o conteúdo textual de um controle baseado em texto.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clientes, entendendo o modelo de objeto de texto de automação de interface
- clientes, controles baseados em texto
- clientes, intervalos de texto
- clientes, padrão de controle de texto
- clientes, padrão de controle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635515"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="87285-108">Compreendendo o modelo de objeto de texto de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="87285-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="87285-109">Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft acessam o conteúdo textual de um controle baseado em texto.</span><span class="sxs-lookup"><span data-stu-id="87285-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="87285-110">Modelo de objeto específico de controle</span><span class="sxs-lookup"><span data-stu-id="87285-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="87285-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87285-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="87285-112">Controles baseados em texto expõem conteúdo textual para aplicativos cliente de automação da interface do usuário por meio de um modelo de objeto de texto simples.</span><span class="sxs-lookup"><span data-stu-id="87285-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="87285-113">Os aplicativos cliente têm acesso ao modelo de objeto de texto por meio das interfaces de padrão de controle [Text e TextRange](uiauto-about-text-and-textrange-patterns.md) , incluindo [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span><span class="sxs-lookup"><span data-stu-id="87285-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="87285-114">Os aplicativos cliente podem usar essas interfaces para recuperar conteúdo textual, atributos de texto e objetos incorporados, como tabelas e hiperlinks, de controles baseados em texto.</span><span class="sxs-lookup"><span data-stu-id="87285-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="87285-115">Os tipos de controle que dão suporte ao modelo de objeto de texto de automação da interface do usuário incluem os tipos de controle [Editar](uiauto-supporteditcontroltype.md) e [documento](uiauto-supportdocumentcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="87285-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="87285-116">Outros tipos de controle, como [ToolTip](uiauto-supporttooltipcontroltype.md) e [Text](uiauto-supporttextcontroltype.md) , também podem oferecer suporte ao modelo de objeto de texto, mas não são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="87285-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="87285-117">O modelo de objeto de texto de automação da interface do usuário não fornece um meio para inserir ou modificar texto.</span><span class="sxs-lookup"><span data-stu-id="87285-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="87285-118">No entanto, alguns controles permitem que o texto seja inserido ou modificado por meio da interface [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) ou por meio de entrada de teclado direta.</span><span class="sxs-lookup"><span data-stu-id="87285-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="87285-119">Modelo de objeto específico de controle</span><span class="sxs-lookup"><span data-stu-id="87285-119">Control-specific Object Model</span></span>

<span data-ttu-id="87285-120">Um controle baseado em texto que implementa seu próprio Modelo de Objeto do Documento (DOM) pode expor o DOM implementando o padrão de controle [ObjectModel](uiauto-implementingobjectmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="87285-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="87285-121">Expor o DOM pode fornecer aos aplicativos cliente maior acesso e controle sobre o conteúdo de um controle baseado em texto.</span><span class="sxs-lookup"><span data-stu-id="87285-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="87285-122">Um aplicativo cliente pode descobrir se um determinado controle baseado em texto implementa um DOM recuperando a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) do controle.</span><span class="sxs-lookup"><span data-stu-id="87285-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="87285-123">Em seguida, chame o método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , especificando o identificador da propriedade [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) e uma variante que receberá true se o controle implementar um dom.</span><span class="sxs-lookup"><span data-stu-id="87285-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="87285-124">Para acessar o DOM, chame o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando o identificador de padrão de controle [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) e uma variável que recebe a interface [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) .</span><span class="sxs-lookup"><span data-stu-id="87285-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="87285-125">Chame o método [**IUIAutomationObjectModelPattern:: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) para recuperar a interface dom.</span><span class="sxs-lookup"><span data-stu-id="87285-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87285-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87285-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87285-127">Padrões de controle Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="87285-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="87285-128">Suporte à automação da interface do usuário para conteúdo textual</span><span class="sxs-lookup"><span data-stu-id="87285-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="87285-129">Trabalhando com controles baseados em texto</span><span class="sxs-lookup"><span data-stu-id="87285-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




