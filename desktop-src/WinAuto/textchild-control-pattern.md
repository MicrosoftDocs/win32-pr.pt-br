---
title: Padrão de controle textchild
description: Apresenta diretrizes e convenções para implementar ITextChildProvider, incluindo informações sobre propriedades e métodos. O padrão de controle textchild é usado para acessar o ancestral mais próximo de um elemento que dá suporte ao padrão de controle de texto.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Automação da interface do usuário, implementando padrão de controle textchild
- Automação da interface do usuário, padrão de controle textfilho
- Automação da interface do usuário, ITextChildProvider
- ITextChildProvider
- Implementando padrões de controle textchild da automação da interface do usuário
- Padrões de controle textchild
- padrões de controle, ITextChildProvider
- padrões de controle, implementando a automação da interface do usuário
- padrões de controle, textchild
- interfaces, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641763"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="73ff5-114">Padrão de controle textchild</span><span class="sxs-lookup"><span data-stu-id="73ff5-114">TextChild Control Pattern</span></span>

<span data-ttu-id="73ff5-115">Apresenta diretrizes e convenções para implementar [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="73ff5-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="73ff5-116">O padrão de controle **textchild** é usado para acessar o ancestral mais próximo de um elemento que dá suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="73ff5-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="73ff5-117">Por exemplo, suponha que o texto em um documento contenha uma imagem inserida e um hiperlink, conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="73ff5-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![captura de tela mostrando o texto que contém uma imagem inserida e um hiperlink](images/textchild-pattern.png)

<span data-ttu-id="73ff5-119">Se você usar as ferramentas de automação da interface do usuário da Microsoft para examinar a árvore de automação da interface do usuário desse conteúdo do documento, ele poderá mostrar um elemento de documento com um elemento filho que representa a imagem e outro elemento filho que representa o hiperlink.</span><span class="sxs-lookup"><span data-stu-id="73ff5-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="73ff5-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="73ff5-120">For example:</span></span>

![captura de tela mostrando inspecionar relatórios um exemplo de árvore de elementos de automação da interface do usuário](images/textchild-pattern-tree.png)

<span data-ttu-id="73ff5-122">Normalmente, o elemento Document no exemplo anterior dá suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , mas os dois filhos do elemento Document não.</span><span class="sxs-lookup"><span data-stu-id="73ff5-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="73ff5-123">Se um aplicativo cliente de automação da interface do usuário tiver uma referência ao elemento Image ou ao elemento Hyperlink, o cliente poderá usar o padrão de controle **textchild** como uma maneira conveniente de acessar o padrão TextControl exposto pelo elemento de documento que o contém.</span><span class="sxs-lookup"><span data-stu-id="73ff5-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="73ff5-124">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="73ff5-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="73ff5-125">Ao implementar a interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="73ff5-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="73ff5-126">A propriedade [**ITextChildProvider:: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) deve especificar o elemento ancestral mais próximo que dá suporte à interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , independentemente de os elementos mais altos na cadeia ancestral também oferecerem suporte a **ITextProvider**.</span><span class="sxs-lookup"><span data-stu-id="73ff5-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="73ff5-127">Um elemento não deve dar suporte à interface [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) e [ITextChildProvider \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="73ff5-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="73ff5-128">Um elemento que implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) deve ser um filho, ou descendente, de um elemento que implementa [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span><span class="sxs-lookup"><span data-stu-id="73ff5-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="73ff5-129">Não é necessário que esse elemento também implemente o [padrão de controle de texto](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span><span class="sxs-lookup"><span data-stu-id="73ff5-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="73ff5-130">A propriedade [**ITextChildProvider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) deve especificar o mesmo intervalo de texto que o elemento do provedor de texto que o contém retorna quando sua função [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) é chamada com o elemento filho Text como o elemento filho incluído.</span><span class="sxs-lookup"><span data-stu-id="73ff5-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="73ff5-131">Membros necessários para **ITextChildProvider**</span><span class="sxs-lookup"><span data-stu-id="73ff5-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="73ff5-132">Essas propriedades e métodos são necessários para implementar a interface [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="73ff5-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="73ff5-133">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="73ff5-133">Required members</span></span>                                                     | <span data-ttu-id="73ff5-134">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="73ff5-134">Member type</span></span> | <span data-ttu-id="73ff5-135">Observações</span><span class="sxs-lookup"><span data-stu-id="73ff5-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="73ff5-136">**TextContainer**</span><span class="sxs-lookup"><span data-stu-id="73ff5-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="73ff5-137">Propriedade</span><span class="sxs-lookup"><span data-stu-id="73ff5-137">Property</span></span>    | <span data-ttu-id="73ff5-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73ff5-138">None</span></span>  |
| [<span data-ttu-id="73ff5-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="73ff5-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="73ff5-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="73ff5-140">Property</span></span>    | <span data-ttu-id="73ff5-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73ff5-141">None</span></span>  |



 

<span data-ttu-id="73ff5-142">Este padrão de controle não tem nenhum método ou evento associado.</span><span class="sxs-lookup"><span data-stu-id="73ff5-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73ff5-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73ff5-143">Related topics</span></span>

<span data-ttu-id="73ff5-144">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="73ff5-144">**Conceptual**</span></span>

- [<span data-ttu-id="73ff5-145">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="73ff5-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="73ff5-146">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="73ff5-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="73ff5-147">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="73ff5-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)