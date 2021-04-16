---
title: Biblioteca de controle do Windows Ribbon Framework
description: Os tópicos contidos nesta seção descrevem o conjunto de controles incluídos no Windows Ribbon Framework. Os controles listados aqui são os objetos de interface do usuário em uma faixa de faixas que expõem a funcionalidade do comando.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105786947"
---
# <a name="windows-ribbon-framework-control-library"></a><span data-ttu-id="a3f1c-104">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="a3f1c-104">Windows Ribbon Framework Control Library</span></span>

<span data-ttu-id="a3f1c-105">Os tópicos contidos nesta seção descrevem o conjunto de controles incluídos no Windows Ribbon Framework.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-105">The topics contained in this section describe the set of controls that are included with the Windows Ribbon framework.</span></span> <span data-ttu-id="a3f1c-106">Os controles listados aqui são os objetos de interface do usuário em uma faixa de faixas que expõem a funcionalidade do comando.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-106">The controls listed here are the UI objects in a ribbon that expose Command functionality.</span></span>

-   [<span data-ttu-id="a3f1c-107">Introdução</span><span class="sxs-lookup"><span data-stu-id="a3f1c-107">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="a3f1c-108">Os controles</span><span class="sxs-lookup"><span data-stu-id="a3f1c-108">The Controls</span></span>](#windows-ribbon-framework-control-library)
    -   [<span data-ttu-id="a3f1c-109">Controles básicos</span><span class="sxs-lookup"><span data-stu-id="a3f1c-109">Basic Controls</span></span>](#basic-controls)
    -   [<span data-ttu-id="a3f1c-110">Controles de contêiner</span><span class="sxs-lookup"><span data-stu-id="a3f1c-110">Container Controls</span></span>](#container-controls)
    -   [<span data-ttu-id="a3f1c-111">Controles especializados</span><span class="sxs-lookup"><span data-stu-id="a3f1c-111">Specialized Controls</span></span>](#specialized-controls)
-   [<span data-ttu-id="a3f1c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3f1c-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="a3f1c-113">Introdução</span><span class="sxs-lookup"><span data-stu-id="a3f1c-113">Introduction</span></span>

<span data-ttu-id="a3f1c-114">A estrutura da faixa de faixas é composta de componentes como [guias](windowsribbon-controls-tab.md) e a [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md), que funcionam em conjunto para fornecer uma experiência de interface do usuário rica.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-114">The Ribbon framework is composed of components such as [Tabs](windowsribbon-controls-tab.md) and the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md), that work together to deliver a rich UI experience.</span></span> <span data-ttu-id="a3f1c-115">Individualmente, esses componentes expõem tipos diferentes de comandos para proporcionar aos clientes uma experiência organizada e previsível em aplicativos de faixa de das faixas.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-115">Individually, these components expose different types of Commands to give customers an organized, predictable experience across Ribbon applications.</span></span> <span data-ttu-id="a3f1c-116">Por exemplo, cada guia expõe comandos relacionados à criação e à ação de partes específicas do conteúdo no espaço de trabalho do aplicativo, enquanto o [menu do aplicativo](windowsribbon-controls-applicationmenu.md) expõe a funcionalidade relacionada a um projeto completo, como um documento, imagem ou filme inteiro.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-116">For example, each Tab exposes Commands related to creating and acting on specific parts of the content within the application workspace, whereas the [Application Menu](windowsribbon-controls-applicationmenu.md) exposes functionality related to a complete project, such as an entire document, picture, or movie.</span></span>

<span data-ttu-id="a3f1c-117">Este tópico fornece uma lista abrangente de controles de faixa de faixas e inclui uma breve descrição de cada controle, com links para uma documentação mais detalhada, quando disponível.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-117">This topic provides a comprehensive list of Ribbon controls and includes a brief description for each control, with links to more detailed documentation where available.</span></span>

## <a name="the-controls"></a><span data-ttu-id="a3f1c-118">Os controles</span><span class="sxs-lookup"><span data-stu-id="a3f1c-118">The Controls</span></span>

<span data-ttu-id="a3f1c-119">A estrutura da faixa de visão é composta de duas [exibições](windowsribbon-reference-elements-view.md): a exibição [**da faixa**](windowsribbon-element-ribbon.md) de forma e a exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="a3f1c-119">The Ribbon framework is composed of two [Views](windowsribbon-reference-elements-view.md): the [**Ribbon**](windowsribbon-element-ribbon.md) View and the [**ContextPopup**](windowsribbon-element-contextpopup.md) View.</span></span> <span data-ttu-id="a3f1c-120">Cada exibição pode hospedar vários componentes que atuam como contêineres de apresentação para todos os controles que são renderizados e gerenciados pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-120">Each View can host several components that act as presentation containers for all controls that are rendered and managed by the framework.</span></span>

<span data-ttu-id="a3f1c-121">A exibição [**da faixa**](windowsribbon-element-ribbon.md) de opções hospeda o elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , o elemento [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) e a barra de comandos da faixa de opções, enquanto a exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) hospeda um elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , um elemento [**Minibarra**](windowsribbon-element-minitoolbar.md) ou ambos.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-121">The [**Ribbon**](windowsribbon-element-ribbon.md) View hosts the [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element, [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) element, and ribbon command bar while the [**ContextPopup**](windowsribbon-element-contextpopup.md) View hosts a [**ContextMenu**](windowsribbon-element-contextmenu.md) element, a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element, or both.</span></span>

<span data-ttu-id="a3f1c-122">Cada controle de estrutura é diferenciado pela funcionalidade associada ao seu [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span><span class="sxs-lookup"><span data-stu-id="a3f1c-122">Each framework control is distinguished by the functionality associated with its [**Command type**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).</span></span>

### <a name="basic-controls"></a><span data-ttu-id="a3f1c-123">Controles básicos</span><span class="sxs-lookup"><span data-stu-id="a3f1c-123">Basic Controls</span></span>

<span data-ttu-id="a3f1c-124">Os controles básicos consistem em um ou mais botões que podem ser invocados por um único clique do mouse para executar uma ação simples.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-124">Basic controls consist of one or more buttons that can be invoked by a single mouse click to perform a simple action.</span></span>

> [!Note]  
> <span data-ttu-id="a3f1c-125">O [**controle giratório**](windowsribbon-element-spinner.md) é uma exceção, pois contém um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-125">The [**Spinner**](windowsribbon-element-spinner.md) is an exception as it contains an edit control.</span></span>

 

<span data-ttu-id="a3f1c-126">A tabela a seguir lista os controles básicos na estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-126">The following table lists the basic controls in the Ribbon framework.</span></span>



| <span data-ttu-id="a3f1c-127">Control</span><span class="sxs-lookup"><span data-stu-id="a3f1c-127">Control</span></span>                                                  | <span data-ttu-id="a3f1c-128">Elemento de marcação</span><span class="sxs-lookup"><span data-stu-id="a3f1c-128">Markup Element</span></span>                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="a3f1c-129">Botão</span><span class="sxs-lookup"><span data-stu-id="a3f1c-129">Button</span></span>](windowsribbon-controls-button.md)              | [<span data-ttu-id="a3f1c-130">**Button**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-130">**Button**</span></span>](windowsribbon-element-button.md)             |
| [<span data-ttu-id="a3f1c-131">Caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="a3f1c-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)         | [<span data-ttu-id="a3f1c-132">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-132">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)         |
| [<span data-ttu-id="a3f1c-133">Botão ajuda</span><span class="sxs-lookup"><span data-stu-id="a3f1c-133">Help Button</span></span>](windowsribbon-controls-helpbutton.md)     | [<span data-ttu-id="a3f1c-134">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-134">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)     |
| [<span data-ttu-id="a3f1c-135">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="a3f1c-135">Spinner</span></span>](windowsribbon-controls-spinner.md)            | [<span data-ttu-id="a3f1c-136">**Controle giratório**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-136">**Spinner**</span></span>](windowsribbon-element-spinner.md)           |
| [<span data-ttu-id="a3f1c-137">Botão de alternância</span><span class="sxs-lookup"><span data-stu-id="a3f1c-137">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md) | [<span data-ttu-id="a3f1c-138">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-138">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a><span data-ttu-id="a3f1c-139">Controles de contêiner</span><span class="sxs-lookup"><span data-stu-id="a3f1c-139">Container Controls</span></span>

<span data-ttu-id="a3f1c-140">Os controles de contêiner são compostos por grupos de controles, menus, listas ou coleções de comandos e itens.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-140">Container controls are composed of groups of controls, menus, lists, or item and Command collections.</span></span>

<span data-ttu-id="a3f1c-141">A estrutura distingue entre dois tipos de contêineres, estático e dinâmico.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-141">The framework distinguishes between two types of containers, static and dynamic.</span></span>

### <a name="static-containers"></a><span data-ttu-id="a3f1c-142">Contêineres estáticos</span><span class="sxs-lookup"><span data-stu-id="a3f1c-142">Static Containers</span></span>

<span data-ttu-id="a3f1c-143">Os contêineres estáticos são declarados e preenchidos, juntamente com todos os recursos associados, no arquivo de marcação da faixa de lista.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-143">Static containers are declared and populated, along with all associated resources, in the Ribbon markup file.</span></span> <span data-ttu-id="a3f1c-144">Esses controles não podem ser modificados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-144">These controls cannot be modified at run time.</span></span>

<span data-ttu-id="a3f1c-145">As vantagens dos controles estáticos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a3f1c-145">The advantages of static controls include the following:</span></span>

-   <span data-ttu-id="a3f1c-146">Rápida criando protótipos.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-146">Rapid prototyping.</span></span> <span data-ttu-id="a3f1c-147">Os controles estáticos possibilitam a criação rápida de uma simulação de faixa de uma forma semelhante a um design de faixa de forma final que não requer código complicado.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-147">Static controls make it possible to quickly build a Ribbon mock-up resembling a final Ribbon design that requires no complicated code.</span></span>
-   <span data-ttu-id="a3f1c-148">Modificações fáceis.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-148">Easy modifications.</span></span> <span data-ttu-id="a3f1c-149">A maioria dos elementos, atributos, recursos e layouts de controles estáticos pode ser modificada na marcação.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-149">Most elements, attributes, resources, and layouts of static controls can be modified in markup.</span></span>
-   <span data-ttu-id="a3f1c-150">Interface do usuário consistente.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-150">Consistent UI.</span></span> <span data-ttu-id="a3f1c-151">Os aplicativos bem projetados fornecem uma interface do usuário consistente e estável que evita alterações em menus e listas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-151">Well-designed applications provide a consistent and stable UI that avoids changes to menus and lists at run time.</span></span>

<span data-ttu-id="a3f1c-152">A tabela a seguir descreve os controles de contêiner estáticos na estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-152">The following table describes the static container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="a3f1c-153">Control</span><span class="sxs-lookup"><span data-stu-id="a3f1c-153">Control</span></span>                                                        | <span data-ttu-id="a3f1c-154">Elemento de marcação</span><span class="sxs-lookup"><span data-stu-id="a3f1c-154">Markup Element</span></span>                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a3f1c-155">Menu do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a3f1c-155">Application Menu</span></span>](windowsribbon-controls-applicationmenu.md) | [<span data-ttu-id="a3f1c-156">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-156">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md) |
| [<span data-ttu-id="a3f1c-157">Pop-up de contexto</span><span class="sxs-lookup"><span data-stu-id="a3f1c-157">Context Popup</span></span>](windowsribbon-controls-contextpopup.md)       | [<span data-ttu-id="a3f1c-158">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-158">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)       |
| [<span data-ttu-id="a3f1c-159">Botão suspenso</span><span class="sxs-lookup"><span data-stu-id="a3f1c-159">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)  | [<span data-ttu-id="a3f1c-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)   |
| [<span data-ttu-id="a3f1c-161">Grupo</span><span class="sxs-lookup"><span data-stu-id="a3f1c-161">Group</span></span>](windowsribbon-controls-group.md)                      | [<span data-ttu-id="a3f1c-162">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-162">**Group**</span></span>](windowsribbon-element-group.md)                     |
| [<span data-ttu-id="a3f1c-163">Grupo de menus</span><span class="sxs-lookup"><span data-stu-id="a3f1c-163">Menu Group</span></span>](windowsribbon-controls-menugroup.md)             | [<span data-ttu-id="a3f1c-164">**Grupo Backstage**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-164">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)             |
| [<span data-ttu-id="a3f1c-165">Botão de divisão</span><span class="sxs-lookup"><span data-stu-id="a3f1c-165">Split Button</span></span>](windowsribbon-controls-splitbutton.md)         | [<span data-ttu-id="a3f1c-166">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-166">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)         |
| [<span data-ttu-id="a3f1c-167">Tab</span><span class="sxs-lookup"><span data-stu-id="a3f1c-167">Tab</span></span>](windowsribbon-controls-tab.md)                          | [<span data-ttu-id="a3f1c-168">**Tab**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-168">**Tab**</span></span>](windowsribbon-element-tab.md)                         |
| [<span data-ttu-id="a3f1c-169">Grupo de guias</span><span class="sxs-lookup"><span data-stu-id="a3f1c-169">Tab Group</span></span>](windowsribbon-controls-tabgroup.md)               | [<span data-ttu-id="a3f1c-170">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-170">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a><span data-ttu-id="a3f1c-171">Contêineres dinâmicos</span><span class="sxs-lookup"><span data-stu-id="a3f1c-171">Dynamic Containers</span></span>

<span data-ttu-id="a3f1c-172">Os contêineres dinâmicos são declarados no arquivo de marcação da faixa de lista.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-172">Dynamic containers are declared in the Ribbon markup file.</span></span> <span data-ttu-id="a3f1c-173">Eles apresentam um grupo de itens ou comandos que são criados ou modificados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-173">They feature a group of items or Commands that are created or modified at run time.</span></span>

<span data-ttu-id="a3f1c-174">Uma subclasse de contêineres dinâmicos, chamadas galerias, é diferenciada por sua implementação da interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="a3f1c-174">A subclass of dynamic containers, called galleries, are distinguished by their implementation of the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="a3f1c-175">Essa interface permite que um controle exponha seu item ou lista de comandos como uma coleção e para dar suporte a atualizações com base na interação do usuário e nas condições de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-175">This interface allows a control to expose its item or Command list as a collection, and to support updates based on both user interaction and run-time conditions.</span></span> <span data-ttu-id="a3f1c-176">Para obter mais informações, consulte [trabalhando com galerias](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="a3f1c-176">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="a3f1c-177">A tabela a seguir lista os controles de contêiner dinâmicos na estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-177">The following table lists the dynamic container controls in the Ribbon framework.</span></span>



| <span data-ttu-id="a3f1c-178">Control</span><span class="sxs-lookup"><span data-stu-id="a3f1c-178">Control</span></span>                                                               | <span data-ttu-id="a3f1c-179">Elemento de marcação</span><span class="sxs-lookup"><span data-stu-id="a3f1c-179">Markup Element</span></span>                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a3f1c-180">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="a3f1c-180">Combo Box</span></span>](windowsribbon-controls-combobox.md)                      | [<span data-ttu-id="a3f1c-181">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-181">**ComboBox**</span></span>](windowsribbon-element-combobox.md)                     |
| [<span data-ttu-id="a3f1c-182">Galeria suspensa</span><span class="sxs-lookup"><span data-stu-id="a3f1c-182">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)       | [<span data-ttu-id="a3f1c-183">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-183">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       |
| [<span data-ttu-id="a3f1c-184">Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="a3f1c-184">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)       | [<span data-ttu-id="a3f1c-185">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-185">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       |
| [<span data-ttu-id="a3f1c-186">Barra de ferramentas de acesso rápido</span><span class="sxs-lookup"><span data-stu-id="a3f1c-186">Quick Access Toolbar</span></span>](windowsribbon-controls-quickaccesstoolbar.md) | [<span data-ttu-id="a3f1c-187">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-187">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md) |
| [<span data-ttu-id="a3f1c-188">Itens recentes</span><span class="sxs-lookup"><span data-stu-id="a3f1c-188">Recent Items</span></span>](windowsribbon-controls-recentitems.md)                | [<span data-ttu-id="a3f1c-189">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-189">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)               |
| [<span data-ttu-id="a3f1c-190">Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="a3f1c-190">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md) | [<span data-ttu-id="a3f1c-191">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-191">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a><span data-ttu-id="a3f1c-192">Controles especializados</span><span class="sxs-lookup"><span data-stu-id="a3f1c-192">Specialized Controls</span></span>

<span data-ttu-id="a3f1c-193">A estrutura da faixa de das faixas contém vários controles especializados para a funcionalidade específica da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-193">The Ribbon framework contains a number of specialized controls for specific UI functionality.</span></span>

<span data-ttu-id="a3f1c-194">A tabela a seguir lista os controles especializados na estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="a3f1c-194">The following table lists the specialized controls in the Ribbon framework.</span></span>



| <span data-ttu-id="a3f1c-195">Control</span><span class="sxs-lookup"><span data-stu-id="a3f1c-195">Control</span></span>                                                                  | <span data-ttu-id="a3f1c-196">Elemento de marcação</span><span class="sxs-lookup"><span data-stu-id="a3f1c-196">Markup Element</span></span>                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="a3f1c-197">Seletor de cores suspensa</span><span class="sxs-lookup"><span data-stu-id="a3f1c-197">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | [<span data-ttu-id="a3f1c-198">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-198">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md) |
| [<span data-ttu-id="a3f1c-199">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="a3f1c-199">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | [<span data-ttu-id="a3f1c-200">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="a3f1c-200">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="a3f1c-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3f1c-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3f1c-202">Noções básicas sobre comandos e controles</span><span class="sxs-lookup"><span data-stu-id="a3f1c-202">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 