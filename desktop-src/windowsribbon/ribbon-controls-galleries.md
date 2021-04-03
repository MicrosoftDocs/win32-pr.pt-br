---
title: Trabalhando com galerias
description: O Windows Ribbon Framework fornece aos desenvolvedores um modelo robusto e consistente para o gerenciamento de conteúdo dinâmico em uma variedade de controles baseados em coleção.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Faixa de das, galerias do Windows
- Faixa de, galerias
- Faixa de, controle DropDownGallery do Windows
- Faixa de, controle DropDownGallery
- Faixa de, controle SplitButtonGallery do Windows
- Faixa de, controle SplitButtonGallery
- Controle DropDownGallery
- Controle SplitButtonGallery
- Faixa de das galerias do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 784c69b0cf23edad906fbb35ee9a2a45454eacea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641582"
---
# <a name="working-with-galleries"></a><span data-ttu-id="2a00a-112">Trabalhando com galerias</span><span class="sxs-lookup"><span data-stu-id="2a00a-112">Working with Galleries</span></span>

<span data-ttu-id="2a00a-113">O Windows Ribbon Framework fornece aos desenvolvedores um modelo robusto e consistente para o gerenciamento de conteúdo dinâmico em uma variedade de controles baseados em coleção.</span><span class="sxs-lookup"><span data-stu-id="2a00a-113">The Windows Ribbon framework provides developers with a robust and consistent model for managing dynamic content across a variety of collection-based controls.</span></span> <span data-ttu-id="2a00a-114">Ao adaptar e reconfigurar a interface do usuário da faixa de opções, esses controles dinâmicos permitem que a estrutura responda à interação do usuário tanto no aplicativo host quanto na faixa de opções e forneça a flexibilidade para lidar com vários ambientes de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2a00a-114">By adapting and reconfiguring the Ribbon UI, these dynamic controls allow the framework to respond to user interaction in both the host application and Ribbon itself, and provide the flexibility to handle various run time environments.</span></span>

-   [<span data-ttu-id="2a00a-115">Introdução</span><span class="sxs-lookup"><span data-stu-id="2a00a-115">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="2a00a-116">Galerias</span><span class="sxs-lookup"><span data-stu-id="2a00a-116">Galleries</span></span>](#working-with-galleries)
    -   [<span data-ttu-id="2a00a-117">Galerias de itens</span><span class="sxs-lookup"><span data-stu-id="2a00a-117">Item Galleries</span></span>](#item-galleries)
    -   [<span data-ttu-id="2a00a-118">Galerias de comandos</span><span class="sxs-lookup"><span data-stu-id="2a00a-118">Command Galleries</span></span>](#command-galleries)
    -   [<span data-ttu-id="2a00a-119">Controles da Galeria</span><span class="sxs-lookup"><span data-stu-id="2a00a-119">Gallery Controls</span></span>](#working-with-galleries)
-   [<span data-ttu-id="2a00a-120">Como implementar uma galeria</span><span class="sxs-lookup"><span data-stu-id="2a00a-120">How to Implement a Gallery</span></span>](#how-to-implement-a-gallery)
    -   [<span data-ttu-id="2a00a-121">Os componentes básicos</span><span class="sxs-lookup"><span data-stu-id="2a00a-121">The Basic Components</span></span>](#the-basic-components)
    -   [<span data-ttu-id="2a00a-122">Declarar os controles na marcação</span><span class="sxs-lookup"><span data-stu-id="2a00a-122">Declare the Controls in Markup</span></span>](#declare-the-controls-in-markup)
    -   [<span data-ttu-id="2a00a-123">Criar um manipulador de comandos</span><span class="sxs-lookup"><span data-stu-id="2a00a-123">Create a Command Handler</span></span>](#create-a-command-handler)
    -   [<span data-ttu-id="2a00a-124">Associar o manipulador de comandos</span><span class="sxs-lookup"><span data-stu-id="2a00a-124">Bind the Command Handler</span></span>](#bind-the-command-handler)
    -   [<span data-ttu-id="2a00a-125">Inicializar uma coleção</span><span class="sxs-lookup"><span data-stu-id="2a00a-125">Initialize a Collection</span></span>](#initialize-a-collection)
    -   [<span data-ttu-id="2a00a-126">Manipular eventos de coleta</span><span class="sxs-lookup"><span data-stu-id="2a00a-126">Handle Collection Events</span></span>](#handle-collection-events)
-   [<span data-ttu-id="2a00a-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a00a-127">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="2a00a-128">Introdução</span><span class="sxs-lookup"><span data-stu-id="2a00a-128">Introduction</span></span>

<span data-ttu-id="2a00a-129">Essa capacidade da estrutura da faixa de opções se adaptar dinamicamente às condições de tempo de execução, aos requisitos de aplicativos e à entrada do usuário final realça os recursos avançados da interface do usuário da estrutura e fornece aos desenvolvedores a flexibilidade de atender a uma ampla gama de necessidades do cliente.</span><span class="sxs-lookup"><span data-stu-id="2a00a-129">This ability of the Ribbon framework to dynamically adapt to run-time conditions, application requirements, and end-user input highlights the rich UI capabilities of the framework, and provides developers with the flexibility to cater to a broad range of customer needs.</span></span>

<span data-ttu-id="2a00a-130">O foco deste guia é descrever os controles da Galeria dinâmica com suporte da estrutura, explicar suas diferenças, discutir quando e onde eles podem ser usados melhor e demonstrar como eles podem ser incorporados a um aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="2a00a-130">The focus of this guide is to describe the dynamic gallery controls supported by the framework, explain their differences, discuss when and where they may best be used, and demonstrate how they can be incorporated into a Ribbon application.</span></span>

## <a name="galleries"></a><span data-ttu-id="2a00a-131">Galerias</span><span class="sxs-lookup"><span data-stu-id="2a00a-131">Galleries</span></span>

<span data-ttu-id="2a00a-132">As galerias são controles de caixa de listagem de forma funcional e graficamente ricos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-132">Galleries are functionally and graphically rich list box controls.</span></span> <span data-ttu-id="2a00a-133">A coleção de itens de uma galeria pode ser organizada por categorias, exibidas em layouts baseados em colunas flexíveis e em linhas, representadas com imagens e texto, e dependendo do tipo de galeria, suporte à visualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="2a00a-133">The item collection of a gallery can be organized by categories, displayed in flexible column and row-based layouts, represented with images and text, and depending on the type of gallery, support live previewing.</span></span>

<span data-ttu-id="2a00a-134">As galerias são funcionalmente diferentes de outros controles de faixa de opções dinâmicos pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="2a00a-134">Galleries are functionally distinct from other dynamic Ribbon controls for the following reasons:</span></span>

-   <span data-ttu-id="2a00a-135">As galerias implementam a interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) que define os vários métodos para manipular coleções de itens da galeria.</span><span class="sxs-lookup"><span data-stu-id="2a00a-135">Galleries implement the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface that defines the various methods for manipulating gallery item collections.</span></span>
-   <span data-ttu-id="2a00a-136">As galerias podem ser atualizadas em tempo de execução, com base na atividade que ocorre diretamente na faixa de, por exemplo, quando um usuário adiciona um comando à barra de ferramentas de acesso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="2a00a-136">Galleries can be updated at run time, based on activity that occurs directly in the Ribbon, such as when a user adds a Command to the Quick Access Toolbar (QAT).</span></span>
-   <span data-ttu-id="2a00a-137">As galerias podem ser atualizadas em tempo de execução, com base na atividade que ocorre indiretamente no ambiente de tempo de execução, como quando um driver de impressora dá suporte apenas a layouts de página de retrato.</span><span class="sxs-lookup"><span data-stu-id="2a00a-137">Galleries can be updated at run time, based on activity that occurs indirectly from the run-time environment, such as when a printer driver supports portrait page layouts only.</span></span>
-   <span data-ttu-id="2a00a-138">As galerias podem ser atualizadas em tempo de execução, com base na atividade que ocorre indiretamente no aplicativo host, como quando um usuário seleciona um item em um documento.</span><span class="sxs-lookup"><span data-stu-id="2a00a-138">Galleries can be updated at run time, based on activity that occurs indirectly in the host application, such as when a user selects an item in a document.</span></span>

<span data-ttu-id="2a00a-139">A estrutura da faixa de faixas expõe dois tipos de galerias: galerias de itens e galerias de comandos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-139">The Ribbon framework exposes two types of galleries: item galleries and Command galleries.</span></span>

### <a name="item-galleries"></a><span data-ttu-id="2a00a-140">Galerias de itens</span><span class="sxs-lookup"><span data-stu-id="2a00a-140">Item Galleries</span></span>

<span data-ttu-id="2a00a-141">As galerias de itens contêm uma coleção baseada em índice de itens relacionados, em que cada item é representado por uma imagem, uma cadeia de caracteres ou ambos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-141">Item galleries contain an index-based collection of related items where each item is represented by an image, a string, or both.</span></span> <span data-ttu-id="2a00a-142">O controle está associado a um único manipulador de comando que se baseia no valor de índice que é identificado pela [propriedade \_ PKEY \_ SelectedItem da interface do usuário](windowsribbon-reference-properties-uipkey-selecteditem.md) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-142">The control is bound to a single Command handler that relies on the index value that is identified by the [UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) property.</span></span>

<span data-ttu-id="2a00a-143">As galerias de itens dão suporte à visualização dinâmica, o que significa exibir um resultado de comando, com base em mouseover ou Focus, sem confirmar ou realmente invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-143">Item galleries support live previewing, which means displaying a Command result, based on mouseover or focus, without committing to or actually invoking the Command.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a00a-144">A estrutura não oferece suporte a galerias de itens de hospedagem no menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a00a-144">The framework does not support hosting item galleries in the Application Menu.</span></span>

 

### <a name="command-galleries"></a><span data-ttu-id="2a00a-145">Galerias de comandos</span><span class="sxs-lookup"><span data-stu-id="2a00a-145">Command Galleries</span></span>

<span data-ttu-id="2a00a-146">As galerias de comandos contêm uma coleção de itens distintos não indexados.</span><span class="sxs-lookup"><span data-stu-id="2a00a-146">Command galleries contain a collection of distinct, non-indexed items.</span></span> <span data-ttu-id="2a00a-147">Cada item é representado por um único controle associado a um manipulador de comando por meio de uma ID de comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-147">Each item is represented by a single control bound to a Command handler through a Command ID.</span></span> <span data-ttu-id="2a00a-148">Como controles autônomos, cada item em uma galeria de comandos roteia eventos de entrada para um manipulador de comandos associado — a Galeria de comandos em si não escuta eventos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-148">Like standalone controls, each item in a Command gallery routes input events to an associated Command handler—the Command gallery itself does not listen for events.</span></span>

<span data-ttu-id="2a00a-149">As galerias de comandos não dão suporte à visualização dinâmica.</span><span class="sxs-lookup"><span data-stu-id="2a00a-149">Command galleries do not support live previewing.</span></span>

### <a name="gallery-controls"></a><span data-ttu-id="2a00a-150">Controles da Galeria</span><span class="sxs-lookup"><span data-stu-id="2a00a-150">Gallery Controls</span></span>

<span data-ttu-id="2a00a-151">Há quatro controles de galeria na estrutura da faixa de faixas: [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)e [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="2a00a-151">There are four gallery controls in the Ribbon framework: the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), and the [**ComboBox**](windowsribbon-element-combobox.md).</span></span> <span data-ttu-id="2a00a-152">Tudo, exceto a **ComboBox** , pode ser implementado como uma galeria de itens ou uma galeria de comandos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-152">All except the **ComboBox** can be implemented as either an item gallery or a Command gallery.</span></span>

### <a name="dropdowngallery"></a><span data-ttu-id="2a00a-153">DropDownGallery</span><span class="sxs-lookup"><span data-stu-id="2a00a-153">DropDownGallery</span></span>

<span data-ttu-id="2a00a-154">Um [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) é um botão que exibe uma lista suspensa que contém uma coleção de itens ou comandos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-154">A [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) is a button that displays a drop-down list that contains a collection of mutually exclusive items or Commands.</span></span>

<span data-ttu-id="2a00a-155">A captura de tela a seguir ilustra o controle da [Galeria suspensa](windowsribbon-controls-dropdowngallery.md) da faixa de opções no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a00a-155">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle de galeria suspensa no Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a><span data-ttu-id="2a00a-157">SplitButtonGallery</span><span class="sxs-lookup"><span data-stu-id="2a00a-157">SplitButtonGallery</span></span>

<span data-ttu-id="2a00a-158">Um [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) é um controle composto que expõe um único item ou comando padrão de sua coleção em um botão primário e exibe outros itens ou comandos em uma lista suspensa mutuamente exclusiva que é exibida quando um botão secundário é clicado.</span><span class="sxs-lookup"><span data-stu-id="2a00a-158">A [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) is a composite control that exposes a single default item or Command from its collection on a primary button, and displays other items or commands in a mutually exclusive drop-down list that is displayed when a secondary button is clicked.</span></span>

<span data-ttu-id="2a00a-159">A captura de tela a seguir ilustra o controle da [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) da faixa de opções no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a00a-159">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle de galeria de botões de divisão no Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a><span data-ttu-id="2a00a-161">InRibbonGallery</span><span class="sxs-lookup"><span data-stu-id="2a00a-161">InRibbonGallery</span></span>

<span data-ttu-id="2a00a-162">Um [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) é uma galeria que exibe uma coleção de itens ou comandos relacionados na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="2a00a-162">An [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is a gallery that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="2a00a-163">Se houver muitos itens na Galeria, será fornecida uma seta de expansão para exibir o restante da coleção em um painel expandido.</span><span class="sxs-lookup"><span data-stu-id="2a00a-163">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

<span data-ttu-id="2a00a-164">A captura de tela a seguir ilustra o controle da [Galeria de faixa de](windowsribbon-controls-inribbongallery.md) opções no Microsoft Paint para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a00a-164">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![captura de tela de um controle da galeria na faixa de faixas na faixa de bits do Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a><span data-ttu-id="2a00a-166">ComboBox</span><span class="sxs-lookup"><span data-stu-id="2a00a-166">ComboBox</span></span>

<span data-ttu-id="2a00a-167">Uma [**ComboBox**](windowsribbon-element-combobox.md) é uma caixa de listagem de coluna única que contém uma coleção de itens com um controle estático ou um controle de edição e uma seta suspensa.</span><span class="sxs-lookup"><span data-stu-id="2a00a-167">A [**ComboBox**](windowsribbon-element-combobox.md) is a single-column list box that contains a collection of items with either a static control or edit control and dropdown arrow.</span></span> <span data-ttu-id="2a00a-168">A parte da caixa de listagem do controle é exibida quando o usuário clica na seta suspensa.</span><span class="sxs-lookup"><span data-stu-id="2a00a-168">The list box portion of the control is displayed when the user clicks the drop-down arrow.</span></span>

<span data-ttu-id="2a00a-169">A captura de tela a seguir ilustra um controle de [caixa de combinação](windowsribbon-controls-combobox.md) da faixa de opções do Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="2a00a-169">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![captura de tela de um controle ComboBox na faixa de faixas do Microsoft Paint.](images/controls/combobox.png)

<span data-ttu-id="2a00a-171">Como a [**ComboBox**](windowsribbon-element-combobox.md) é exclusivamente uma galeria de itens, ela não oferece suporte a itens de comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-171">Because the [**ComboBox**](windowsribbon-element-combobox.md) is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="2a00a-172">Ele também é o único controle de galeria que não oferece suporte a um espaço de comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-172">It is also the only gallery control that does not support a Command Space.</span></span> <span data-ttu-id="2a00a-173">(Um espaço de comando é uma coleção de comandos que são declarados em marcação e listados na parte inferior de uma galeria de itens ou galeria de comandos.)</span><span class="sxs-lookup"><span data-stu-id="2a00a-173">(A Command Space is a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery.)</span></span>

<span data-ttu-id="2a00a-174">O exemplo de código a seguir mostra a marcação necessária para declarar um espaço de comando de três botões em um [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="2a00a-174">The following code example shows the markup required to declare a three-button Command Space in a [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



<span data-ttu-id="2a00a-175">A captura de tela a seguir ilustra o espaço de comando de três botões do exemplo de código anterior.</span><span class="sxs-lookup"><span data-stu-id="2a00a-175">The following screen shot illustrates the three-button Command Space of the preceding code example.</span></span>

![captura de tela de um espaço de comando de três botões em um dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a><span data-ttu-id="2a00a-177">Como implementar uma galeria</span><span class="sxs-lookup"><span data-stu-id="2a00a-177">How to Implement a Gallery</span></span>

<span data-ttu-id="2a00a-178">Esta seção aborda os detalhes de implementação das galerias de faixa de das faixas e explica como incorporá-las em um aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="2a00a-178">This section discusses the implementation details of Ribbon galleries and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="the-basic-components"></a><span data-ttu-id="2a00a-179">Os componentes básicos</span><span class="sxs-lookup"><span data-stu-id="2a00a-179">The Basic Components</span></span>

<span data-ttu-id="2a00a-180">Esta seção descreve o conjunto de propriedades e métodos que formam o backbone do conteúdo dinâmico na estrutura da faixa de opção e dão suporte à adição, exclusão, atualização e à manipulação do conteúdo e do layout visual de galerias de faixa de opção em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2a00a-180">This section describes the set of properties and methods that form the backbone of dynamic content in the Ribbon framework and support adding, deleting, updating, and otherwise manipulating the content and visual layout of Ribbon galleries at run time.</span></span>

### <a name="iuicollection"></a><span data-ttu-id="2a00a-181">IUICollection</span><span class="sxs-lookup"><span data-stu-id="2a00a-181">IUICollection</span></span>

<span data-ttu-id="2a00a-182">As galerias exigem um conjunto básico de métodos para acessar e manipular os itens individuais em suas coleções.</span><span class="sxs-lookup"><span data-stu-id="2a00a-182">Galleries require a basic set of methods to access and manipulate the individual items in their collections.</span></span>

<span data-ttu-id="2a00a-183">A interface [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) define esses métodos, e a estrutura complementa sua funcionalidade com métodos adicionais que são definidos na interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-183">The [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) interface defines these methods, and the framework supplements their functionality with additional methods that are defined in the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface.</span></span> <span data-ttu-id="2a00a-184">O **IUICollection** é implementado pela estrutura para cada declaração da galeria na marcação da faixa de medida.</span><span class="sxs-lookup"><span data-stu-id="2a00a-184">**IUICollection** is implemented by the framework for each gallery declaration in the Ribbon markup.</span></span>

<span data-ttu-id="2a00a-185">Se for necessária uma funcionalidade adicional que não seja fornecida pela interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , um objeto de coleção personalizado implementado pelo aplicativo host e derivado de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) poderá ser substituído pela coleção de estruturas.</span><span class="sxs-lookup"><span data-stu-id="2a00a-185">If additional functionality is required that is not provided by the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) interface, then a custom collection object that is implemented by the host application and derived from [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) can be substituted for the framework collection.</span></span>

### <a name="iuicollectionchangedevent"></a><span data-ttu-id="2a00a-186">IUICollectionChangedEvent</span><span class="sxs-lookup"><span data-stu-id="2a00a-186">IUICollectionChangedEvent</span></span>

<span data-ttu-id="2a00a-187">Para que um aplicativo responda às alterações em uma coleção da galeria, ele deve implementar a interface [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-187">For an application to respond to changes in a gallery collection, it must implement the [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) interface.</span></span> <span data-ttu-id="2a00a-188">Os aplicativos podem assinar notificações de um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio do ouvinte de eventos [**IUICollectionChangedEvent:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-188">Applications can subscribe to notifications from an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [**IUICollectionChangedEvent::OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) event listener.</span></span>

<span data-ttu-id="2a00a-189">Quando o aplicativo substitui a coleção da Galeria fornecida pela estrutura por uma coleção personalizada, o aplicativo deve implementar a interface [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-189">When the application replaces the gallery collection provided by the framework with a custom collection, the application should implement the [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface.</span></span> <span data-ttu-id="2a00a-190">Se [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) não for implementado, o aplicativo não poderá notificar a estrutura das alterações na coleção personalizada que exigem atualizações dinâmicas para o controle da galeria.</span><span class="sxs-lookup"><span data-stu-id="2a00a-190">If [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, then the application is unable to notify the framework of changes in the custom collection that require dynamic updates to the gallery control.</span></span>

<span data-ttu-id="2a00a-191">Nesses casos em que [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) não está implementado, o controle galeria só pode ser atualizado por meio de invalidação por meio de [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) e [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)ou chamando [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="2a00a-191">In those cases where [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) is not implemented, the gallery control can be updated only by invalidation through [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) and [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty), or by calling [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>

### <a name="iuisimplepropertyset"></a><span data-ttu-id="2a00a-192">IUISimplePropertySet</span><span class="sxs-lookup"><span data-stu-id="2a00a-192">IUISimplePropertySet</span></span>

<span data-ttu-id="2a00a-193">Os aplicativos devem implementar IUISimplePropertySet para cada item ou comando em uma coleção da galeria.</span><span class="sxs-lookup"><span data-stu-id="2a00a-193">Applications must implement IUISimplePropertySet for each item or Command in a gallery collection.</span></span> <span data-ttu-id="2a00a-194">No entanto, as propriedades que podem ser solicitadas com [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) variam.</span><span class="sxs-lookup"><span data-stu-id="2a00a-194">However, the properties that can be requested with [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) vary.</span></span>

<span data-ttu-id="2a00a-195">Os itens são definidos e vinculados a uma Galeria por meio da chave de propriedade [ \_ PKEY \_ ItemsSource da interface do usuário](windowsribbon-reference-properties-uipkey-itemssource.md) e expõem propriedades com um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-195">Items are defined and bound to a gallery through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key and expose properties with an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="2a00a-196">As propriedades válidas para itens em galerias de itens ([**\_ \_ coleção de COMMANDTYPE de interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a00a-196">The valid properties for items in item galleries ([**UI\_COMMANDTYPE\_COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="2a00a-197">Algumas propriedades de item, como [o \_ \_ rótulo PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md), podem ser definidas na marcação.</span><span class="sxs-lookup"><span data-stu-id="2a00a-197">Some item properties, such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), can be defined in markup.</span></span> <span data-ttu-id="2a00a-198">Para obter mais detalhes, consulte a documentação de referência de [chaves de propriedade](windowsribbon-reference-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-198">For more detail, see the [Property Keys](windowsribbon-reference-properties.md) reference documentation.</span></span>

 



<span data-ttu-id="2a00a-199">Control</span><span class="sxs-lookup"><span data-stu-id="2a00a-199">Control</span></span>

<span data-ttu-id="2a00a-200">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a00a-200">Properties</span></span>

[<span data-ttu-id="2a00a-201">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="2a00a-201">**ComboBox**</span></span>](windowsribbon-element-combobox.md)

<span data-ttu-id="2a00a-202">[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-202">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="2a00a-203">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2a00a-203">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)

<span data-ttu-id="2a00a-204">[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY, \_ MyImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-204">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="2a00a-205">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="2a00a-205">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)

<span data-ttu-id="2a00a-206">[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY, \_ MyImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-206">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

[<span data-ttu-id="2a00a-207">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2a00a-207">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)

<span data-ttu-id="2a00a-208">[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY, \_ MyImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-208">[UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), [UI\_PKEY\_ItemImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>

<span data-ttu-id="2a00a-209">[Interface do usuário \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) é uma propriedade da Galeria de itens.</span><span class="sxs-lookup"><span data-stu-id="2a00a-209">[UI\_PKEY\_SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) is a property of the item gallery.</span></span>



 

<span data-ttu-id="2a00a-210">As propriedades de item válidas para galerias de comando ([**interface do usuário de \_ COMMANDTYPE \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a00a-210">The valid item properties for Command galleries ([**UI\_COMMANDTYPE\_COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) are described in the following table.</span></span>



| <span data-ttu-id="2a00a-211">Control</span><span class="sxs-lookup"><span data-stu-id="2a00a-211">Control</span></span>                                                                | <span data-ttu-id="2a00a-212">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2a00a-212">Properties</span></span>                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a00a-213">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="2a00a-213">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)       | <span data-ttu-id="2a00a-214">[Interface do usuário \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [interface do usuário \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-214">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="2a00a-215">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="2a00a-215">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)       | <span data-ttu-id="2a00a-216">[Interface do usuário \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [interface do usuário \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-216">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span> |
| [<span data-ttu-id="2a00a-217">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="2a00a-217">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md) | <span data-ttu-id="2a00a-218">[Interface do usuário \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [interface do usuário \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)</span><span class="sxs-lookup"><span data-stu-id="2a00a-218">[UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md)</span></span>  |



 

<span data-ttu-id="2a00a-219">As categorias são usadas para organizar itens e comandos em galerias.</span><span class="sxs-lookup"><span data-stu-id="2a00a-219">Categories are used to organize items and Commands in galleries.</span></span> <span data-ttu-id="2a00a-220">As categorias são definidas e associadas a uma Galeria por meio da chave de propriedade [ \_ \_ categorias de PKEY de interface do usuário](windowsribbon-reference-properties-uipkey-categories.md) e expõem propriedades com um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) específico à categoria.</span><span class="sxs-lookup"><span data-stu-id="2a00a-220">Categories are defined and bound to a gallery through the [UI\_PKEY\_Categories](windowsribbon-reference-properties-uipkey-categories.md) property key and expose properties with a category-specific [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="2a00a-221">As categorias não têm um CommandType e não dão suporte à interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2a00a-221">Categories do not have a CommandType and do not support user interaction.</span></span> <span data-ttu-id="2a00a-222">Por exemplo, as categorias não podem se tornar SelectedItem em uma galeria de itens e não estão associadas a um comando em uma galeria de comandos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-222">For example, categories cannot become the SelectedItem in an item gallery, and they are not bound to a Command in a Command gallery.</span></span> <span data-ttu-id="2a00a-223">Assim como outras propriedades de item da galeria, as propriedades de categoria, como o [ \_ \_ rótulo PKEY da interface do](windowsribbon-reference-properties-uipkey-label.md) usuário e a [interface do usuário \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) , podem ser recuperadas chamando [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span><span class="sxs-lookup"><span data-stu-id="2a00a-223">Like other gallery item properties, category properties such as [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md) and [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) can be retrieved by calling [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a00a-224">[**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) deve retornar [**a \_ coleção \_ de interface do usuário INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) quando a [interface do usuário \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) é solicitada para um item que não tem uma categoria associada.</span><span class="sxs-lookup"><span data-stu-id="2a00a-224">[**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) should return [**UI\_COLLECTION\_INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) when [UI\_PKEY\_CategoryId](windowsribbon-reference-properties-uipkey-categoryid.md) is requested for an item that does not have an associated category.</span></span>

 

### <a name="declare-the-controls-in-markup"></a><span data-ttu-id="2a00a-225">Declarar os controles na marcação</span><span class="sxs-lookup"><span data-stu-id="2a00a-225">Declare the Controls in Markup</span></span>

<span data-ttu-id="2a00a-226">As galerias, como todos os controles de faixa de faixas, devem ser declaradas na marcação.</span><span class="sxs-lookup"><span data-stu-id="2a00a-226">Galleries, like all Ribbon controls, must be declared in markup.</span></span> <span data-ttu-id="2a00a-227">Uma galeria é identificada na marcação como uma galeria de itens ou galeria de comandos e vários detalhes de apresentação são declarados.</span><span class="sxs-lookup"><span data-stu-id="2a00a-227">A gallery is identified in markup as an item gallery or Command gallery, and various presentation details are declared.</span></span> <span data-ttu-id="2a00a-228">Ao contrário de outros controles, as galerias exigem somente o controle base ou o contêiner de coleção para serem declarados na marcação.</span><span class="sxs-lookup"><span data-stu-id="2a00a-228">Unlike other controls, galleries require the base control only, or collection container, to be declared in markup.</span></span> <span data-ttu-id="2a00a-229">As coleções reais são populadas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="2a00a-229">The actual collections are populated at run time.</span></span> <span data-ttu-id="2a00a-230">Quando uma galeria é declarada em marcação, o atributo *Type* é usado para especificar se a galeria é uma galeria de itens de uma galeria de comandos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-230">When a gallery is declared in markup, the *Type* attribute is used to specify whether the gallery is an item gallery of a Command gallery.</span></span>

<span data-ttu-id="2a00a-231">Há vários atributos de layout opcionais disponíveis para cada um dos controles discutidos aqui.</span><span class="sxs-lookup"><span data-stu-id="2a00a-231">There are a number of optional layout attributes available for each of the controls discussed here.</span></span> <span data-ttu-id="2a00a-232">Esses atributos fornecem preferências do desenvolvedor para a estrutura seguir que afetam diretamente como um controle é populado e exibido em uma faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="2a00a-232">These attributes provide developer preferences for the framework to follow that directly affect how a control is populated and displayed in a ribbon.</span></span> <span data-ttu-id="2a00a-233">As preferências aplicáveis na marcação estão relacionadas aos modelos de exibição e de layout e aos comportamentos discutidos na [personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="2a00a-233">The preferences applicable in markup are related to the display and layout templates and behaviors discussed in [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="2a00a-234">Se um controle específico não permitir preferências de layout diretamente na marcação ou se as preferências de layout não forem especificadas, a estrutura definirá as convenções de exibição específicas do controle com base na quantidade de espaço disponível na tela.</span><span class="sxs-lookup"><span data-stu-id="2a00a-234">If a particular control does not allow layout preferences directly in markup, or the layout preferences are not specified, then the framework defines control-specific display conventions based on the amount of screen space available.</span></span>

<span data-ttu-id="2a00a-235">Os exemplos a seguir demonstram como incorporar um conjunto de galerias em uma faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="2a00a-235">The following examples demonstrate how to incorporate a set of galleries into a Ribbon.</span></span>

### <a name="command-declarations"></a><span data-ttu-id="2a00a-236">Declarações de comando</span><span class="sxs-lookup"><span data-stu-id="2a00a-236">Command Declarations</span></span>

<span data-ttu-id="2a00a-237">Os comandos devem ser declarados com um atributo *CommandName* que é usado para associar um controle ou conjunto de controles, com o comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-237">Commands should be declared with a *CommandName* attribute that is used to associate a control, or set of controls, with the Command.</span></span>

<span data-ttu-id="2a00a-238">Um atributo *CommandID* usado para associar um comando a um manipulador de comando quando a marcação é compilada também pode ser especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="2a00a-238">A *CommandId* attribute used to bind a Command to a Command handler when the markup is compiled can also be specified here.</span></span> <span data-ttu-id="2a00a-239">Se nenhuma ID for fornecida, uma será gerada pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="2a00a-239">If no ID is provided, then one is generated by the framework.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a><span data-ttu-id="2a00a-240">Declarações de controle</span><span class="sxs-lookup"><span data-stu-id="2a00a-240">Control Declarations</span></span>

<span data-ttu-id="2a00a-241">Esta seção contém exemplos que demonstram a marcação de controle básico necessária para os vários tipos de galeria.</span><span class="sxs-lookup"><span data-stu-id="2a00a-241">This section contains examples that demonstrate the basic control markup required for the various gallery types.</span></span> <span data-ttu-id="2a00a-242">Eles mostram como declarar os controles da galeria e associá-los a um comando por meio do atributo *CommandName* .</span><span class="sxs-lookup"><span data-stu-id="2a00a-242">They show how to declare the gallery controls and associate them with a Command through the *CommandName* attribute.</span></span>

<span data-ttu-id="2a00a-243">O exemplo a seguir mostra uma declaração de controle para o [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) em que o atributo *Type* é usado para especificar que esta é uma galeria de comandos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-243">The following example shows a control declaration for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) where the *Type* attribute is used to specify that this is a Command gallery.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



<span data-ttu-id="2a00a-244">O exemplo a seguir mostra uma declaração de controle para o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="2a00a-244">The following example shows a control declaration for the [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



<span data-ttu-id="2a00a-245">O exemplo a seguir mostra uma declaração de controle para o [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="2a00a-245">The following example shows a control declaration for the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).</span></span>

> [!Note]  
> <span data-ttu-id="2a00a-246">Como o [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) foi projetado para exibir um subconjunto de sua coleção de itens na faixa de opção sem ativar um menu suspenso, ele fornece vários atributos opcionais que regem seu tamanho e o layout do item na inicialização da faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="2a00a-246">Because the [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) is designed to display a subset of its item collection in the Ribbon without activating a drop-down menu, it provides a number of optional attributes that govern its size and item layout on Ribbon initialization.</span></span> <span data-ttu-id="2a00a-247">Esses atributos são exclusivos do **InRibbonGallery** e não estão disponíveis nos outros controles dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-247">These attributes are unique to the **InRibbonGallery** and are not available from the other dynamic controls.</span></span>

 


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



<span data-ttu-id="2a00a-248">O exemplo a seguir mostra uma declaração de controle para a [**ComboBox**](windowsribbon-element-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="2a00a-248">The following example shows a control declaration for the [**ComboBox**](windowsribbon-element-combobox.md).</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a><span data-ttu-id="2a00a-249">Criar um manipulador de comandos</span><span class="sxs-lookup"><span data-stu-id="2a00a-249">Create a Command Handler</span></span>

<span data-ttu-id="2a00a-250">Para cada comando, a estrutura da faixa de faixas requer um manipulador de comandos correspondente no aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="2a00a-250">For each Command, the Ribbon framework requires a corresponding Command handler in the host application.</span></span> <span data-ttu-id="2a00a-251">Os manipuladores de comandos são implementados pelo aplicativo host da faixa de faixas e são derivados da interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-251">Command handlers are implemented by the Ribbon host application and are derived from the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span>

> [!Note]  
> <span data-ttu-id="2a00a-252">Vários comandos podem ser associados a um único manipulador de comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-252">Multiple Commands can be bound to a single Command handler.</span></span>

 

<span data-ttu-id="2a00a-253">Um manipulador de comandos tem duas finalidades:</span><span class="sxs-lookup"><span data-stu-id="2a00a-253">A Command handler serves two purposes:</span></span>

-   <span data-ttu-id="2a00a-254">[**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responde às solicitações de atualização de propriedade.</span><span class="sxs-lookup"><span data-stu-id="2a00a-254">[**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responds to property update requests.</span></span> <span data-ttu-id="2a00a-255">Os valores das propriedades de comando, como [interface do usuário \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md) ou [ \_ \_ rótulo de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md), são definidos por meio de chamadas para [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) ou [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="2a00a-255">The values of Command properties, such as [UI\_PKEY\_Enabled](windowsribbon-reference-properties-uipkey-enabled.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md), are set through calls to [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) or [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span>
-   <span data-ttu-id="2a00a-256">[**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responde a executar eventos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-256">[**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responds to execute events.</span></span> <span data-ttu-id="2a00a-257">Esse método dá suporte aos três Estados de execução a seguir que são especificados pelo parâmetro [**\_ EXECUTIONVERB da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .</span><span class="sxs-lookup"><span data-stu-id="2a00a-257">This method supports the following three execution states that are specified by the [**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) parameter.</span></span>
    -   <span data-ttu-id="2a00a-258">O estado de execução é executado ou confirma todos os comandos aos quais o manipulador está associado.</span><span class="sxs-lookup"><span data-stu-id="2a00a-258">The Execute state executes, or commits to, any commands to which the handler is bound.</span></span>
    -   <span data-ttu-id="2a00a-259">O estado de visualização visualiza todos os comandos aos quais o manipulador está associado.</span><span class="sxs-lookup"><span data-stu-id="2a00a-259">The Preview state previews any commands to which the handler is bound.</span></span> <span data-ttu-id="2a00a-260">Isso essencialmente executa os comandos sem confirmar o resultado.</span><span class="sxs-lookup"><span data-stu-id="2a00a-260">This essentially executes the commands without committing to the result.</span></span>
    -   <span data-ttu-id="2a00a-261">O estado CancelPreview cancela qualquer comando visualizado.</span><span class="sxs-lookup"><span data-stu-id="2a00a-261">The CancelPreview state cancels any previewed Commands.</span></span> <span data-ttu-id="2a00a-262">Isso é necessário para dar suporte à passagem por meio de um menu ou lista e Visualizar sequencialmente e desfazer os resultados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="2a00a-262">This is required to support traversal through a menu or list and sequentially preview and undo the results as required.</span></span>

<span data-ttu-id="2a00a-263">O exemplo a seguir demonstra um manipulador de comando da galeria.</span><span class="sxs-lookup"><span data-stu-id="2a00a-263">The following example demonstrates a gallery command handler.</span></span>


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a><span data-ttu-id="2a00a-264">Associar o manipulador de comandos</span><span class="sxs-lookup"><span data-stu-id="2a00a-264">Bind the Command Handler</span></span>

<span data-ttu-id="2a00a-265">Depois de definir um manipulador de comando, o comando deve ser associado ao manipulador.</span><span class="sxs-lookup"><span data-stu-id="2a00a-265">After you define a Command handler, the Command must be bound to the handler.</span></span>

<span data-ttu-id="2a00a-266">O exemplo a seguir demonstra como associar um comando da galeria a um manipulador de comandos específico.</span><span class="sxs-lookup"><span data-stu-id="2a00a-266">The following example demonstrates how to bind a gallery Command to a specific Command handler.</span></span> <span data-ttu-id="2a00a-267">Nesse caso, os controles [**ComboBox**](windowsribbon-element-combobox.md) e Gallery são associados aos respectivos manipuladores de comandos.</span><span class="sxs-lookup"><span data-stu-id="2a00a-267">In this case, both the [**ComboBox**](windowsribbon-element-combobox.md) and gallery controls are bound to their respective Command handlers.</span></span>


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a><span data-ttu-id="2a00a-268">Inicializar uma coleção</span><span class="sxs-lookup"><span data-stu-id="2a00a-268">Initialize a Collection</span></span>

<span data-ttu-id="2a00a-269">O exemplo a seguir demonstra uma implementação personalizada de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para galerias de item e de comando.</span><span class="sxs-lookup"><span data-stu-id="2a00a-269">The following example demonstrates a custom implementation of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) for both item and Command galleries.</span></span>

<span data-ttu-id="2a00a-270">A classe CItemProperties neste exemplo é derivada de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span><span class="sxs-lookup"><span data-stu-id="2a00a-270">The CItemProperties class in this example is derived from [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset).</span></span> <span data-ttu-id="2a00a-271">Além do método necessário [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), a classe CItemProperties implementa um conjunto de funções auxiliares para o rastreamento de inicialização e de índice.</span><span class="sxs-lookup"><span data-stu-id="2a00a-271">In addition to the required method [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), the CItemProperties class implements a set of helper functions for initialization and index tracking.</span></span>


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a><span data-ttu-id="2a00a-272">Manipular eventos de coleta</span><span class="sxs-lookup"><span data-stu-id="2a00a-272">Handle Collection Events</span></span>

<span data-ttu-id="2a00a-273">O exemplo a seguir demonstra uma implementação de IUICollectionChangedEvent.</span><span class="sxs-lookup"><span data-stu-id="2a00a-273">The following example demonstrates an IUICollectionChangedEvent implementation.</span></span>


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="2a00a-274">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a00a-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a00a-275">Propriedades da coleção</span><span class="sxs-lookup"><span data-stu-id="2a00a-275">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="2a00a-276">Criando um aplicativo de faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="2a00a-276">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="2a00a-277">Noções básicas sobre comandos e controles</span><span class="sxs-lookup"><span data-stu-id="2a00a-277">Understanding Commands and Controls</span></span>](windowsribbon-commandscontrols.md)
</dt> <dt>

[<span data-ttu-id="2a00a-278">Diretrizes de experiência do usuário da faixa de das</span><span class="sxs-lookup"><span data-stu-id="2a00a-278">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="2a00a-279">Processo de design da faixa de das</span><span class="sxs-lookup"><span data-stu-id="2a00a-279">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[<span data-ttu-id="2a00a-280">Exemplo de galeria</span><span class="sxs-lookup"><span data-stu-id="2a00a-280">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 