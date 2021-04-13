---
title: Declarando comandos e controles com marcação de faixa de medida
description: O Windows Ribbon Framework usa uma linguagem de marcação baseada em linguagem XAML (XAML) para implementar de forma declarativa a aparência de um aplicativo da faixa de faixas.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Faixa de medida do Windows, estrutura de marcação
- Faixa de faixas, estrutura de marcação
- Faixa de-se do Windows, separando a apresentação da lógica de comando
- Faixa de faixas, separando a apresentação da lógica de comando
- Faixa de, componentes do Windows
- Faixa de, componentes
- sistema de comandos para Windows Ribbon
- controles para a faixa de faixas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366436"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a><span data-ttu-id="f11de-111">Declarando comandos e controles com marcação de faixa de medida</span><span class="sxs-lookup"><span data-stu-id="f11de-111">Declaring Commands and Controls with Ribbon Markup</span></span>

<span data-ttu-id="f11de-112">O Windows Ribbon Framework usa uma linguagem de marcação baseada em linguagem XAML (XAML) para implementar de forma declarativa a aparência de um aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="f11de-112">The Windows Ribbon framework uses a markup language based on Extensible Application Markup Language (XAML) to declaratively implement the appearance of a Ribbon application.</span></span>

-   [<span data-ttu-id="f11de-113">Separando apresentação da lógica de comando</span><span class="sxs-lookup"><span data-stu-id="f11de-113">Separating Presentation from Command Logic</span></span>](#separating-presentation-from-command-logic)
-   [<span data-ttu-id="f11de-114">Estrutura de marcação</span><span class="sxs-lookup"><span data-stu-id="f11de-114">Markup Structure</span></span>](#markup-structure)
-   [<span data-ttu-id="f11de-115">Componentes da faixa de das</span><span class="sxs-lookup"><span data-stu-id="f11de-115">Ribbon Components</span></span>](#ribbon-components)
-   [<span data-ttu-id="f11de-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f11de-116">Related topics</span></span>](#related-topics)

## <a name="separating-presentation-from-command-logic"></a><span data-ttu-id="f11de-117">Separando apresentação da lógica de comando</span><span class="sxs-lookup"><span data-stu-id="f11de-117">Separating Presentation from Command Logic</span></span>

<span data-ttu-id="f11de-118">A separação dos atributos de apresentação e visuais da lógica de comando na estrutura da faixa de faixas é realizada por meio de duas plataformas de desenvolvimento diferentes, mas dependentes.</span><span class="sxs-lookup"><span data-stu-id="f11de-118">The separation of presentation and visual attributes from command logic in the Ribbon framework is accomplished through two distinct, but dependent, development platforms.</span></span> <span data-ttu-id="f11de-119">Layouts de controle, comportamentos de dimensionamento, declarações de comando e especificações de recursos são o domínio de tempo de design de uma sintaxe de marcação declarativa com base na especificação de [linguagem XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) .</span><span class="sxs-lookup"><span data-stu-id="f11de-119">Control layouts, scaling behaviors, Command declarations, and resource specifications are the design time domain of a declarative markup syntax based on the [Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) specification.</span></span> <span data-ttu-id="f11de-120">Funcionalidade de nível baixo, ganchos de aplicativo e manipuladores de comando são definidos em implementações de interface com base em Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="f11de-120">Low level functionality, application hooks, and Command handlers are defined in Component Object Model (COM)-based interface implementations.</span></span>

<span data-ttu-id="f11de-121">Essa separação de apresentação e lógica oferece os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="f11de-121">This separation of presentation and logic provides the following benefits:</span></span>

-   <span data-ttu-id="f11de-122">Um ciclo de desenvolvimento de aplicativos mais eficiente que permite que desenvolvedores e designers da interface do usuário implementem a GUI do aplicativo da faixa de faixas independentemente da funcionalidade do aplicativo principal.</span><span class="sxs-lookup"><span data-stu-id="f11de-122">A more efficient application development cycle which allows UI developers and designers to implement the GUI of the Ribbon application independently from the core application functionality.</span></span> <span data-ttu-id="f11de-123">Essa funcionalidade básica pode ser deixada para os desenvolvedores de software dedicados.</span><span class="sxs-lookup"><span data-stu-id="f11de-123">This core functionality can be left to dedicated software developers.</span></span>
-   <span data-ttu-id="f11de-124">Manutenção menos dispendiosa porque as alterações na GUI são possíveis sem alterações na funcionalidade básica (e vice-versa).</span><span class="sxs-lookup"><span data-stu-id="f11de-124">Less costly maintenance because changes to the GUI are possible without changes to core functionality (and vice versa).</span></span>
-   <span data-ttu-id="f11de-125">Especificação simples de recursos de cadeia de caracteres e imagem por meio de marcação.</span><span class="sxs-lookup"><span data-stu-id="f11de-125">Simple specification of string and image resources through markup.</span></span>
-   <span data-ttu-id="f11de-126">Facilidade de protótipos.</span><span class="sxs-lookup"><span data-stu-id="f11de-126">Ease of prototyping.</span></span>

## <a name="markup-structure"></a><span data-ttu-id="f11de-127">Estrutura de marcação</span><span class="sxs-lookup"><span data-stu-id="f11de-127">Markup Structure</span></span>

<span data-ttu-id="f11de-128">Existem duas ramificações distintas dentro da estrutura da marcação da estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="f11de-128">Two distinct branches exist within the structure of Ribbon framework markup.</span></span>

<span data-ttu-id="f11de-129">A primeira ramificação contém um manifesto de declarações de comando e recurso (cadeias de caracteres e imagens).</span><span class="sxs-lookup"><span data-stu-id="f11de-129">The first branch contains a manifest of Command and resource declarations (strings and images).</span></span> <span data-ttu-id="f11de-130">Cada entrada de comando é usada pela estrutura para associar um controle da faixa de faixas, por meio de uma ID de comando, a um manipulador de comandos definido no código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f11de-130">Each Command entry is used by the framework to bind a Ribbon control, through a Command ID, to a Command handler defined in the application code.</span></span>

<span data-ttu-id="f11de-131">A segunda ramificação contém as declarações de controle reais.</span><span class="sxs-lookup"><span data-stu-id="f11de-131">The second branch contains the actual control declarations.</span></span> <span data-ttu-id="f11de-132">Cada controle é associado a um comando por meio de um atributo *CommandName* que é mapeado para um atributo de *nome* especificado em cada declaração de comando.</span><span class="sxs-lookup"><span data-stu-id="f11de-132">Each control is associated with a Command through a *CommandName* attribute that maps to a *Name* attribute specified in each Command declaration.</span></span>

## <a name="ribbon-components"></a><span data-ttu-id="f11de-133">Componentes da faixa de das</span><span class="sxs-lookup"><span data-stu-id="f11de-133">Ribbon Components</span></span>

<span data-ttu-id="f11de-134">A funcionalidade da interface do usuário do Framework é exposta por meio de [exibições](windowsribbon-reference-elements-view.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-134">Ribbon framework UI functionality is exposed through [Views](windowsribbon-reference-elements-view.md).</span></span> <span data-ttu-id="f11de-135">Uma exibição é essencialmente um contêiner, como a [**faixa**](windowsribbon-element-ribbon.md) de e- [**ContextPopup**](windowsribbon-element-contextpopup.md), que é usada para apresentar os controles de estrutura e os comandos aos quais eles estão vinculados.</span><span class="sxs-lookup"><span data-stu-id="f11de-135">A View is essentially a container, such as the [**Ribbon**](windowsribbon-element-ribbon.md) and [**ContextPopup**](windowsribbon-element-contextpopup.md), that is used to present framework controls and the Commands they are bound to.</span></span>

<span data-ttu-id="f11de-136">O modo de exibição da [**faixa**](windowsribbon-element-ribbon.md) de visão é composto por vários componentes que incluem um [menu de aplicativo](windowsribbon-controls-applicationmenu.md), a barra de [ferramentas de acesso rápido (qat)](windowsribbon-controls-quickaccesstoolbar.md) para exibir comandos comumente usados da interface do usuário da faixa de [guia, guias](windowsribbon-controls-tab.md) de núcleo e contextual que contêm [grupos](windowsribbon-controls-group.md) de controles e o sistema de menus de contexto avançado do [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-136">The [**Ribbon**](windowsribbon-element-ribbon.md) View is composed of several components that include an [Application Menu](windowsribbon-controls-applicationmenu.md), the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md) for displaying commonly used Commands from the ribbon UI, core and contextual [tabs](windowsribbon-controls-tab.md) that contain [groups](windowsribbon-controls-group.md) of controls, and the rich context menu system of the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

<span data-ttu-id="f11de-137">Todos os componentes da faixa de faixas são declarados em um arquivo de marcação autônomo que:</span><span class="sxs-lookup"><span data-stu-id="f11de-137">All Ribbon components are declared in a standalone markup file that:</span></span>

-   <span data-ttu-id="f11de-138">Especifica as propriedades básicas para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="f11de-138">Specifies the basic properties for each element.</span></span>
-   <span data-ttu-id="f11de-139">Mostra as relações hierárquicas claramente.</span><span class="sxs-lookup"><span data-stu-id="f11de-139">Shows hierarchical relationships clearly.</span></span>
-   <span data-ttu-id="f11de-140">Fornece preferências de layout e dicas de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="f11de-140">Supplies layout preferences and scaling hints.</span></span> <span data-ttu-id="f11de-141">Para obter mais informações sobre modelos de layout da faixa de faixas, consulte [Personalizando uma faixa de opção por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-141">For more information on Ribbon framework layout templates, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>
-   <span data-ttu-id="f11de-142">Fornece uma maneira de definir recursos como imagens e rótulos.</span><span class="sxs-lookup"><span data-stu-id="f11de-142">Provides a way to define resources such as images and labels.</span></span> <span data-ttu-id="f11de-143">Para obter mais informações sobre recursos de imagem, consulte [especificando recursos de imagem da faixa de Ribbon](windowsribbon-imageformats.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-143">For more information on image resources, see [Specifying Ribbon Image Resources](windowsribbon-imageformats.md).</span></span>

<span data-ttu-id="f11de-144">Os dois exemplos de marcação da faixa de opções a seguir demonstram como um conjunto de itens de menu do aplicativo da faixa de opções é associado a um nome de comando e ID.</span><span class="sxs-lookup"><span data-stu-id="f11de-144">The following two Ribbon markup examples demonstrate how a set of Ribbon Application Menu items are each associated with a Command name and ID.</span></span>

1.  <span data-ttu-id="f11de-145">Esta seção mostra as declarações de comando necessárias para um menu de aplicativo com comandos básicos, como novo, abrir e salvar.</span><span class="sxs-lookup"><span data-stu-id="f11de-145">This section shows the Command declarations required for an Application Menu with basic commands such as New, Open, and Save.</span></span>
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  <span data-ttu-id="f11de-146">Esta seção mostra as declarações de controle associadas.</span><span class="sxs-lookup"><span data-stu-id="f11de-146">This section shows the associated Control declarations.</span></span>
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

<span data-ttu-id="f11de-147">Quando a marcação é compilada com a ferramenta UICC (compilador de comando de interface do usuário), os nomes de comando e as IDs são colocados em um arquivo de cabeçalho usado pelo aplicativo host da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="f11de-147">When the markup is compiled with the UI Command Compiler (UICC) tool, the Command names and IDs are placed into a header file used by the Ribbon host application.</span></span>

<span data-ttu-id="f11de-148">Veja a seguir um exemplo de um arquivo de cabeçalho gerado pelo UICC.</span><span class="sxs-lookup"><span data-stu-id="f11de-148">The following is an example of a header file generated by UICC.</span></span>


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a><span data-ttu-id="f11de-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f11de-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11de-150">Linguagem XAML (XAML)</span><span class="sxs-lookup"><span data-stu-id="f11de-150">Extensible Application Markup Language (XAML)</span></span>](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[<span data-ttu-id="f11de-151">Compilando marcação da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="f11de-151">Compiling Ribbon Markup</span></span>](windowsribbon-intentcl.md)
</dt> </dl>

 

 