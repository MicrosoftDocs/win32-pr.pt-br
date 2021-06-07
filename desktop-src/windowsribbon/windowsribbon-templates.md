---
title: Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento
description: Os controles hospedados na barra de comandos da faixa de opções estão sujeitos a regras de layout impostas pela estrutura da Faixa de Opções do Windows e com base em uma combinação de comportamentos padrão e modelos de layout (definidos por estrutura e personalizados), conforme declarado na marcação faixa de opções. Essas regras definem os comportamentos de layout adaptável da estrutura da Faixa de Opções que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opções em tempo de corrida.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Faixa de Opções do Windows, personalização
- Faixa de opções, personalização
- Faixa de Opções do Windows, Modelos sizeDefinition
- Ribbon,SizeDefinition templates
- Faixa de Opções do Windows, modelos personalizados
- Faixa de opções, modelos personalizados
- personalização da Faixa de Opções do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444137"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="ae002-111">Personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="ae002-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="ae002-112">Os controles hospedados na barra de comandos da faixa de opções estão sujeitos a regras de layout impostas pela estrutura da Faixa de Opções do Windows e com base em uma combinação de comportamentos padrão e modelos de layout (definidos por estrutura e personalizados), conforme declarado na marcação faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ae002-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="ae002-113">Essas regras definem os comportamentos de layout adaptável da estrutura da Faixa de Opções que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opções em tempo de corrida.</span><span class="sxs-lookup"><span data-stu-id="ae002-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="ae002-114">Introdução</span><span class="sxs-lookup"><span data-stu-id="ae002-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="ae002-115">Tamanho da Faixa de Opções Modelos de Definição</span><span class="sxs-lookup"><span data-stu-id="ae002-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="ae002-116">Modelos personalizados</span><span class="sxs-lookup"><span data-stu-id="ae002-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="ae002-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae002-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="ae002-118">Introdução</span><span class="sxs-lookup"><span data-stu-id="ae002-118">Introduction</span></span>

<span data-ttu-id="ae002-119">O layout adaptável, conforme definido pela estrutura da Faixa de Opções, é a capacidade de todos os controles na interface do usuário da faixa de opções ajustar dinamicamente sua organização, tamanho, formato e escala relativa com base nas alterações no tamanho da faixa de opções em tempo de executar.</span><span class="sxs-lookup"><span data-stu-id="ae002-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="ae002-120">A estrutura expõe a funcionalidade de layout adaptável por meio de um conjunto de elementos de marcação dedicados a especificar e personalizar vários comportamentos de layout.</span><span class="sxs-lookup"><span data-stu-id="ae002-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="ae002-121">Uma coleção de modelos, chamada [**SizeDefinitions,**](windowsribbon-element-sizedefinition.md)é definida pela estrutura , cada uma com suporte a vários cenários de controle e layout.</span><span class="sxs-lookup"><span data-stu-id="ae002-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="ae002-122">No entanto, a estrutura também dá suporte a modelos personalizados caso os modelos predefinidos não forneçam a experiência da interface do usuário ou os layouts exigidos por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae002-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="ae002-123">Para exibir controles em um layout preferencial em um tamanho de faixa de opções específico, modelos predefinidos e modelos personalizados funcionam em conjunto com o [**elemento ScalingPolicy.**](windowsribbon-element-scalingpolicy.md)</span><span class="sxs-lookup"><span data-stu-id="ae002-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="ae002-124">Esse elemento contém um manifesto de preferências de tamanho que a estrutura usa como um guia ao renderizar a faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ae002-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="ae002-125">A estrutura da Faixa de Opções fornece comportamentos de layout padrão com base em um conjunto de heurísticas internos para a organização e apresentação de controles em tempo de operação sem a necessidade de modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ae002-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="ae002-126">No entanto, essa funcionalidade destina-se apenas a fins de criação de protótipos.</span><span class="sxs-lookup"><span data-stu-id="ae002-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="ae002-127">Tamanho da Faixa de Opções Modelos de Definição</span><span class="sxs-lookup"><span data-stu-id="ae002-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="ae002-128">A estrutura ribbon fornece um conjunto abrangente de modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) que especificam o tamanho e o comportamento de layout para um [grupo de](windowsribbon-controls-group.md) controles de faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ae002-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="ae002-129">Esses modelos abrangem os cenários mais comuns para organizar controles em um aplicativo de Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="ae002-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="ae002-130">Para impor uma experiência de usuário consistente em aplicativos de Faixa de Opções, cada modelo [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impõe restrições aos controles ou à família de controles aos que ele dá suporte.</span><span class="sxs-lookup"><span data-stu-id="ae002-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="ae002-131">Por exemplo, a família de controles de botão inclui:</span><span class="sxs-lookup"><span data-stu-id="ae002-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="ae002-132">Botão</span><span class="sxs-lookup"><span data-stu-id="ae002-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="ae002-133">Botão de alternância</span><span class="sxs-lookup"><span data-stu-id="ae002-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="ae002-134">Botão de lista listada</span><span class="sxs-lookup"><span data-stu-id="ae002-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="ae002-135">Botão Dividir</span><span class="sxs-lookup"><span data-stu-id="ae002-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="ae002-136">Galeria de lista listada</span><span class="sxs-lookup"><span data-stu-id="ae002-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="ae002-137">Galeria de Botões divididos</span><span class="sxs-lookup"><span data-stu-id="ae002-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="ae002-138">Lista Seletor de Cor</span><span class="sxs-lookup"><span data-stu-id="ae002-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="ae002-139">Embora a família de controles de entrada inclua:</span><span class="sxs-lookup"><span data-stu-id="ae002-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="ae002-140">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="ae002-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="ae002-141">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="ae002-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="ae002-142">[A Caixa de](windowsribbon-controls-checkbox.md) Seleção [e a Galeria](windowsribbon-controls-inribbongallery.md) na Faixa de Opções não pertencem à família de botões ou à família de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae002-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="ae002-143">Esses dois controles só podem ser usados quando explicitamente indicados em um [**modelo SizeDefinition.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="ae002-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="ae002-144">Veja a seguir uma lista dos modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) com uma descrição do layout e dos controles permitidos por cada modelo.</span><span class="sxs-lookup"><span data-stu-id="ae002-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae002-145">Se os controles declarados na marcação não mapearem exatamente para o tipo de controle, a ordem e [a](windowsribbon-compilationerrors.md) quantidade definidos no modelo associado, um erro de validação será registrado pelo [compilador](windowsribbon-intentcl.md) de marcação e a compilação será encerrada.</span><span class="sxs-lookup"><span data-stu-id="ae002-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="ae002-146">OneButton</span><span class="sxs-lookup"><span data-stu-id="ae002-146">OneButton</span></span>

<span data-ttu-id="ae002-147">Um controle de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-147">One button-family control.</span></span><br/> <span data-ttu-id="ae002-148">Há suporte apenas para tamanho de grupo grande.</span><span class="sxs-lookup"><span data-stu-id="ae002-148">Only Large group size is supported.</span></span><br/>

![imagem do modelo de sizeefinition onebutton.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="ae002-150">TwoButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-150">TwoButtons</span></span>

<span data-ttu-id="ae002-151">Dois controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-151">Two button-family controls.</span></span><br/> <span data-ttu-id="ae002-152">Há suporte apenas para tamanhos de grupo Grande e Médio.</span><span class="sxs-lookup"><span data-stu-id="ae002-152">Only Large and Medium group sizes are supported.</span></span><br/>

![imagem do modelo de design de tamanho grande de dois botões.](images/overviews/sizedefinition-twobuttons-large.png)

![imagem do modelo de dimensionamento médio de dois botões.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="ae002-155">ThreeButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-155">ThreeButtons</span></span>

<span data-ttu-id="ae002-156">Três controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-156">Three button-family controls.</span></span><br/> <span data-ttu-id="ae002-157">Há suporte apenas para tamanhos de grupo Grande e Médio.</span><span class="sxs-lookup"><span data-stu-id="ae002-157">Only Large and Medium group sizes are supported.</span></span><br/>

![imagem de modelo de projeto de tamanho grande de três botões.](images/overviews/sizedefinition-threebuttons-large.png)

![imagem do modelo de dimensionamento médio de trêsbuttons.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="ae002-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="ae002-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="ae002-161">Três controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-161">Three button-family controls.</span></span><br/> <span data-ttu-id="ae002-162">O primeiro botão é apresentado em destaque em todos os três tamanhos.</span><span class="sxs-lookup"><span data-stu-id="ae002-162">The first button is presented prominently in all three sizes.</span></span><br/>

![imagem do modelo threebuttons-onebtonedtwosmall large sizeefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![imagem do modelo threebuttons-onebtonedtwosmall medium sizeefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![imagem do modelo threebuttons-onebtonedtwosmall small sizeefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="ae002-166">ThreeButtonsAndOneCheckBox</span><span class="sxs-lookup"><span data-stu-id="ae002-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="ae002-167">Três controles de família de botões acompanhados por um único controle CheckBox.</span><span class="sxs-lookup"><span data-stu-id="ae002-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="ae002-168">Há suporte apenas para tamanhos de grupo Grande e Médio.</span><span class="sxs-lookup"><span data-stu-id="ae002-168">Only Large and Medium group sizes are supported.</span></span><br/>

![imagem do modelo threebuttonsandonecheckbox large sizeefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![imagem do modelo de dimensionamento médio threebuttonsandonecheckbox.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="ae002-171">FourButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-171">FourButtons</span></span>

<span data-ttu-id="ae002-172">Quatro controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-172">Four button-family controls.</span></span><br/>

![imagem do modelo de design de tamanho grande de quatro botões.](images/overviews/sizedefinition-fourbuttons-large.png)

![imagem do modelo de dimensionamento médio de quatrobuttons.](images/overviews/sizedefinition-fourbuttons-medium.png)

![imagem do modelo de dimensionamento pequeno de quatro botões.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="ae002-176">FiveButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-176">FiveButtons</span></span>

<span data-ttu-id="ae002-177">Cinco controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-177">Five button-family controls.</span></span><br/>

![imagem do modelo fivebuttons large sizeefinition.](images/overviews/sizedefinition-fivebuttons-large.png)

![imagem do modelo de dimensionamento médio de fivebuttons.](images/overviews/sizedefinition-fivebuttons-medium.png)

![imagem do modelo fivebuttons small sizeefinition.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="ae002-181">FiveOrSixButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-181">FiveOrSixButtons</span></span>

<span data-ttu-id="ae002-182">Cinco controles de família de botões e um sexto botão opcional.</span><span class="sxs-lookup"><span data-stu-id="ae002-182">Five button-family controls and an optional sixth button.</span></span><br/>

![imagem do modelo fiveorsixbuttons large sizeefinition.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![imagem do modelo fiveorsixbuttons medium sizeefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![imagem do modelo fiveorsixbuttons small sizeefinition.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="ae002-186">SixButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-186">SixButtons</span></span>

<span data-ttu-id="ae002-187">Seis controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-187">Six button-family controls.</span></span><br/>

![imagem do modelo de design de tamanho grande de seis botões.](images/overviews/sizedefinition-sixbuttons-large.png)

![imagem do modelo de dimensionamento médio de seis botões.](images/overviews/sizedefinition-sixbuttons-medium.png)

![imagem de modelo de dimensionamento pequeno de seis botões.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="ae002-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="ae002-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="ae002-192">Seis controles de família de botões (apresentação alternativa).</span><span class="sxs-lookup"><span data-stu-id="ae002-192">Six button-family controls (alternate presentation).</span></span><br/>

![imagem do modelo de projeto de dimensionamento grande sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![modelo de dimensionamento médio sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![imagem do modelo de projeto de dimensionamento pequeno sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="ae002-196">SevenButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-196">SevenButtons</span></span>

<span data-ttu-id="ae002-197">Sete controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-197">Seven button-family controls.</span></span><br/>

![imagem do modelo sevenbuttons large sizeefinition.](images/overviews/sizedefinition-sevenbuttons-large.png)

![imagem do modelo sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![imagem do modelo sevenbuttons small sizeefinition.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="ae002-201">EightButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-201">EightButtons</span></span>

<span data-ttu-id="ae002-202">Os oito controles da família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-202">Eight button-family controls.</span></span><br/>

![imagem do modelo eightbuttons-lastthreesmall grande sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Picture of eightbuttons-lastthreesmall Medium sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![imagem do modelo eightbuttons-lastthreesmall Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="ae002-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="ae002-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="ae002-207">Oito botões – controles da família (apresentação alternativa).</span><span class="sxs-lookup"><span data-stu-id="ae002-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="ae002-208">Todos os elementos de controle declarados com este modelo devem estar contidos em dois elementos de [**Control**](windowsribbon-element-controlgroup.md) : um para os cinco primeiros elementos e um para os últimos três elementos.</span><span class="sxs-lookup"><span data-stu-id="ae002-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="ae002-209">O exemplo a seguir demonstra a marcação necessária para este modelo.</span><span class="sxs-lookup"><span data-stu-id="ae002-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![imagem do modelo eightbuttons grande sizedefinition.](images/overviews/sizedefinition-eightbuttons-large.png)

![Picture of eightbuttons Medium sizedefinition template.](images/overviews/sizedefinition-eightbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do eightbuttons.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="ae002-213">NineButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-213">NineButtons</span></span>

<span data-ttu-id="ae002-214">Nove controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-214">Nine button-family controls.</span></span>

![imagem do modelo ninebuttons grande sizedefinition.](images/overviews/sizedefinition-ninebuttons-large.png)

![Picture of ninebuttons Medium sizedefinition template.](images/overviews/sizedefinition-ninebuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do ninebuttons.](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="ae002-218">TenButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-218">TenButtons</span></span>

<span data-ttu-id="ae002-219">Dez controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-219">Ten button-family controls.</span></span>

![imagem do modelo tenbuttons grande sizedefinition.](images/overviews/sizedefinition-tenbuttons-large.png)

![Picture of tenbuttons Medium sizedefinition template.](images/overviews/sizedefinition-tenbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do tenbuttons.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="ae002-223">ElevenButtons</span><span class="sxs-lookup"><span data-stu-id="ae002-223">ElevenButtons</span></span>

<span data-ttu-id="ae002-224">11 botões-controles da família.</span><span class="sxs-lookup"><span data-stu-id="ae002-224">Eleven button-family controls.</span></span>

![imagem do modelo elevenbuttons grande sizedefinition.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Picture of elevenbuttons Medium sizedefinition template.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do elevenbuttons.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="ae002-228">OneFontControl</span><span class="sxs-lookup"><span data-stu-id="ae002-228">OneFontControl</span></span>

<span data-ttu-id="ae002-229">Um [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="ae002-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="ae002-230">Há suporte apenas para tamanhos de grupo grande e médio.</span><span class="sxs-lookup"><span data-stu-id="ae002-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae002-231">A estrutura não oferece suporte à inclusão de um [**FontControl**](windowsribbon-element-fontcontrol.md) em uma definição de modelo personalizado.</span><span class="sxs-lookup"><span data-stu-id="ae002-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![imagem do modelo onefontcontrol grande sizedefinition.](images/overviews/sizedefinition-onefontcontrol-large.png)

![Picture of onefontcontrol Medium sizedefinition template.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="ae002-234">OneInRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="ae002-234">OneInRibbonGallery</span></span>

<span data-ttu-id="ae002-235">Um controle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ae002-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="ae002-236">Há suporte apenas para tamanhos de grupos grandes e pequenos.</span><span class="sxs-lookup"><span data-stu-id="ae002-236">Only Large and Small group sizes are supported.</span></span>

![imagem do modelo oneinribbongallery grande sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![imagem do modelo de sizedefinition pequeno do oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="ae002-239">InRibbonGalleryAndBigButton</span><span class="sxs-lookup"><span data-stu-id="ae002-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="ae002-240">Um controle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) e um controle de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="ae002-241">Há suporte apenas para tamanhos de grupos grandes e pequenos.</span><span class="sxs-lookup"><span data-stu-id="ae002-241">Only Large and Small group sizes are supported.</span></span>

![imagem do modelo inribbongalleryandbigbutton grande sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![imagem do modelo de sizedefinition pequeno do inribbongalleryandbigbutton.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="ae002-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="ae002-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="ae002-245">Um controle [de galeria na faixa de faixas](windowsribbon-controls-inribbongallery.md) e dois ou três controles de família de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="ae002-246">A Galeria recolhe a representação pop-up em tamanhos de grupo médio e pequeno.</span><span class="sxs-lookup"><span data-stu-id="ae002-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![imagem do modelo inribbongalleryandbuttons-galleryscalesfirst grande sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Picture of inribbongalleryandbuttons-galleryscalesfirst Medium sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![imagem do modelo inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="ae002-250">ButtonGroups</span><span class="sxs-lookup"><span data-stu-id="ae002-250">ButtonGroups</span></span>

<span data-ttu-id="ae002-251">Uma organização complexa de controles de família de botão 32 (a maioria deles é opcional).</span><span class="sxs-lookup"><span data-stu-id="ae002-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="ae002-252">Além do botão de tamanho normal opcional do modelo de ButtonGroups grande, todos os elementos de controle declarados com esse modelo devem estar contidos nos elementos do [**controlador de controle**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="ae002-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="ae002-253">O exemplo a seguir demonstra a marcação necessária para exibir todos os elementos de controle de 32 (obrigatórios e opcionais) com este modelo.</span><span class="sxs-lookup"><span data-stu-id="ae002-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![imagem do modelo ButtonGroups grande sizedefinition.](images/overviews/sizedefinition-buttongroups-large.png)

![Picture of ButtonGroups Medium sizedefinition template.](images/overviews/sizedefinition-buttongroups-medium.png)

![imagem do modelo de sizedefinition pequeno do ButtonGroups.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="ae002-257">ButtonGroupsAndInputs</span><span class="sxs-lookup"><span data-stu-id="ae002-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="ae002-258">Dois controles de família de entrada (o segundo é opcional) seguido por uma disposição complexa de 29 botões de família de botão (a maioria deles é opcional).</span><span class="sxs-lookup"><span data-stu-id="ae002-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="ae002-259">Há suporte apenas para tamanhos de grupo grande e médio.</span><span class="sxs-lookup"><span data-stu-id="ae002-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="ae002-260">Todos os elementos de controle declarados com esse modelo devem estar contidos em elementos de [**Control**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="ae002-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="ae002-261">O exemplo a seguir demonstra a marcação necessária para exibir todos os elementos de controle (obrigatórios e opcionais) com este modelo.</span><span class="sxs-lookup"><span data-stu-id="ae002-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![imagem do modelo buttongroupsandinputs grande sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Picture of buttongroupsandinputs Medium sizedefinition template.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="ae002-264">BigButtonsAndSmallButtonsOrInputs</span><span class="sxs-lookup"><span data-stu-id="ae002-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="ae002-265">Dois controles de família de botões (ambos opcionais) seguidos por dois ou três controles de botão ou de família de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae002-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="ae002-266">Há suporte apenas para tamanhos de grupo grande e médio.</span><span class="sxs-lookup"><span data-stu-id="ae002-266">Only Large and Medium group sizes are supported.</span></span>

![imagem do modelo bigbuttonsandsmallbuttonsorinputs grande sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Picture of bigbuttonsandsmallbuttonsorinputs Medium sizedefinition template.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="ae002-269">Exemplo de SizeDefinition básico</span><span class="sxs-lookup"><span data-stu-id="ae002-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="ae002-270">O exemplo de código a seguir fornece uma demonstração básica de como declarar um modelo [**SizeDefinition**](windowsribbon-element-sizedefinition.md) na marcação da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ae002-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="ae002-271">O *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) é usado para esse exemplo específico, mas todos os modelos de estrutura são especificados de maneira semelhante.</span><span class="sxs-lookup"><span data-stu-id="ae002-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="ae002-272">Exemplo de SizeDefinition complexo com políticas de dimensionamento</span><span class="sxs-lookup"><span data-stu-id="ae002-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="ae002-273">O comportamento de recolhimento dos modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pode ser controlado por meio do uso de políticas de dimensionamento na marcação da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="ae002-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="ae002-274">O elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contém um manifesto de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e declarações de [**escala**](windowsribbon-element-scale.md) que especificam preferências de layout adaptável para um ou mais elementos de [**grupo**](windowsribbon-element-group.md) quando a faixa de opções é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="ae002-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="ae002-275">É altamente recomendável que os detalhes da política de dimensionamento adequados sejam especificados de forma que a maioria, se não todos, os elementos do [**grupo**](windowsribbon-element-group.md) sejam associados a um elemento [**Scale**](windowsribbon-element-scale.md) , no qual o atributo *size* é igual a `Popup` .</span><span class="sxs-lookup"><span data-stu-id="ae002-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="ae002-276">Isso permite que a estrutura processe a faixa de opções com o menor tamanho possível e ofereça suporte à maior variedade de dispositivos de vídeo, antes de introduzir automaticamente um mecanismo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ae002-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="ae002-277">O exemplo de código a seguir demonstra um manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica uma preferência de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.</span><span class="sxs-lookup"><span data-stu-id="ae002-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="ae002-278">Modelos personalizados</span><span class="sxs-lookup"><span data-stu-id="ae002-278">Custom Templates</span></span>

<span data-ttu-id="ae002-279">Se os comportamentos de layout padrão e os modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidos não oferecerem a flexibilidade ou o suporte para um cenário de layout específico, os modelos personalizados serão suportados pela estrutura da faixa de opções por meio do elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="ae002-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="ae002-280">Os modelos personalizados podem ser declarados de duas maneiras: um método autônomo usando o elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) para declarar modelos reutilizáveis, nomeados ou um método embutido específico do [**grupo**](windowsribbon-element-group.md).</span><span class="sxs-lookup"><span data-stu-id="ae002-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="ae002-281">Modelo autônomo</span><span class="sxs-lookup"><span data-stu-id="ae002-281">Standalone Template</span></span>

<span data-ttu-id="ae002-282">O exemplo de código a seguir ilustra um modelo personalizado básico e reutilizável.</span><span class="sxs-lookup"><span data-stu-id="ae002-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="ae002-283">Modelo embutido</span><span class="sxs-lookup"><span data-stu-id="ae002-283">Inline Template</span></span>

<span data-ttu-id="ae002-284">Os exemplos de código a seguir ilustram um modelo personalizado embutido básico para um grupo de quatro botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="ae002-285">Esta seção de código mostra as declarações de comando para um grupo de botões.</span><span class="sxs-lookup"><span data-stu-id="ae002-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="ae002-286">Recursos de imagem grandes e pequenos também são especificados aqui.</span><span class="sxs-lookup"><span data-stu-id="ae002-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="ae002-287">Esta seção de código demonstra como definir modelos de [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) grandes, médios e pequenos para exibir os quatro botões em vários tamanhos e layouts.</span><span class="sxs-lookup"><span data-stu-id="ae002-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="ae002-288">A Declaração [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) para a guia define qual modelo é usado para um grupo de controles com base no tamanho da faixa de medida e no espaço exigido pela guia ativa.</span><span class="sxs-lookup"><span data-stu-id="ae002-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="ae002-289">As imagens a seguir mostram como os modelos do exemplo anterior são aplicados à interface do usuário da faixa de opções para acomodar uma diminuição no tamanho da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ae002-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|  <span data-ttu-id="ae002-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae002-290">Type</span></span>  |      <span data-ttu-id="ae002-291">Imagem</span><span class="sxs-lookup"><span data-stu-id="ae002-291">Image</span></span>                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae002-292">Grande</span><span class="sxs-lookup"><span data-stu-id="ae002-292">Large</span></span>  | ![imagem de um modelo personalizado grande embutido.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="ae002-294">Médio</span><span class="sxs-lookup"><span data-stu-id="ae002-294">Medium</span></span> | ![imagem de um modelo personalizado médio embutido.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="ae002-296">Pequeno</span><span class="sxs-lookup"><span data-stu-id="ae002-296">Small</span></span>  | ![imagem de um modelo personalizado pequeno embutido.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="ae002-298">Pop-up</span><span class="sxs-lookup"><span data-stu-id="ae002-298">Popup</span></span>  | ![imagem de um modelo personalizado pop-up embutido.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="ae002-300">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae002-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae002-301">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="ae002-301">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="ae002-302">**Escalonáve**</span><span class="sxs-lookup"><span data-stu-id="ae002-302">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="ae002-303">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="ae002-303">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





