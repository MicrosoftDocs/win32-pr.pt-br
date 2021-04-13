---
title: Noções básicas sobre comandos e controles
description: A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comandos do Windows Ribbon Framework \ 8212; um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Visão geral dos comandos do Windows Ribbon
- Visão geral de comandos
- Visão geral dos controles do Windows
- Visão geral dos controles
- sistema de comandos para Windows Ribbon
- controles para a faixa de faixas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104569239"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="58295-109">Noções básicas sobre comandos e controles</span><span class="sxs-lookup"><span data-stu-id="58295-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="58295-110">A separação da lógica da apresentação é a filosofia do design que inspira o sistema de apresentação de comando da estrutura da faixa de forma do Windows – um sistema baseado em um padrão de design onde a funcionalidade e o comportamento são implementados independentemente dos controles que expõem essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="58295-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="58295-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="58295-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="58295-112">O sistema de comandos da faixa de dasgem do Windows</span><span class="sxs-lookup"><span data-stu-id="58295-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="58295-113">Controles</span><span class="sxs-lookup"><span data-stu-id="58295-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="58295-114">Comandos</span><span class="sxs-lookup"><span data-stu-id="58295-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="58295-115">A experiência de comando em ação</span><span class="sxs-lookup"><span data-stu-id="58295-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="58295-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58295-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="58295-117">Introdução</span><span class="sxs-lookup"><span data-stu-id="58295-117">Introduction</span></span>

<span data-ttu-id="58295-118">Este artigo aborda o design do sistema de comando da estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="58295-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="58295-119">Ele descreve os conceitos de comandos e controles e explora como eles funcionam em conjunto para fornecer uma experiência de comando avançada com uma série de novos recursos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="58295-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="58295-120">O sistema de comandos da faixa de dasgem do Windows</span><span class="sxs-lookup"><span data-stu-id="58295-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="58295-121">Na estrutura da faixa de, os comandos e os controles são entidades independentes.</span><span class="sxs-lookup"><span data-stu-id="58295-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="58295-122">Um comando é uma estrutura abstrata, sem restrições de apresentação, que representa uma tarefa ou classe específica de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="58295-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="58295-123">Um controle, por outro lado, é um objeto concreto que expõe a funcionalidade de comando por meio da interface do usuário da faixa de tipos.</span><span class="sxs-lookup"><span data-stu-id="58295-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="58295-124">Essa distinção fornece a capacidade de definir comandos que são livres de detalhes da interface do usuário e que podem ser executados na intenção de uma ação sem a necessidade de gerenciar como a ação foi invocada.</span><span class="sxs-lookup"><span data-stu-id="58295-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="58295-125">Controles</span><span class="sxs-lookup"><span data-stu-id="58295-125">Controls</span></span>

<span data-ttu-id="58295-126">Os controles são os objetos de interface do usuário necessários para apresentação de comando.</span><span class="sxs-lookup"><span data-stu-id="58295-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="58295-127">Eles são renderizados e gerenciados em tempo de execução pela estrutura com base na interação do usuário e em um conjunto de propriedades e comportamentos inerentes.</span><span class="sxs-lookup"><span data-stu-id="58295-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="58295-128">Conhecido como layout adaptável, a flexibilidade gerenciada pela estrutura da interface do usuário é uma das grandes vantagens da faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="58295-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="58295-129">Os controles da faixa de opção podem se reconfigurar automaticamente por meio de modelos de layout dependentes de estrutura ou definidos pelo desenvolvedor que são capazes de responder a vários requisitos de tempo de execução, tudo sem escrever uma única linha de código de apresentação.</span><span class="sxs-lookup"><span data-stu-id="58295-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="58295-130">Para obter mais informações, consulte [Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="58295-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="58295-131">Além dos benefícios do layout adaptável, vários controles de faixa de opção complexos fornecem soluções independentes para espaços de problema de interface do usuário específicos.</span><span class="sxs-lookup"><span data-stu-id="58295-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="58295-132">Ao oferecer um modelo de interação sofisticado, os controles da faixa de opção, como o FontControl ou o ColorPicker, fornecem a capacidade de manipular dados em termos mais abstratos por meio de bolsas de propriedades de fontes reais ou de atributos de cor, em vez de vários subcontroles, enumerações e valores de índice de controles padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="58295-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="58295-133">Comandos</span><span class="sxs-lookup"><span data-stu-id="58295-133">Commands</span></span>

<span data-ttu-id="58295-134">Rigidamente acoplado aos controles da faixa de faixas que expõem sua funcionalidade, implementações de comando são o domínio do aplicativo host e assumem a forma de ouvintes de eventos, manipuladores de comandos e várias propriedades de comandos.</span><span class="sxs-lookup"><span data-stu-id="58295-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="58295-135">Os comandos são declarados na marcação da faixa de forma com uma ID exclusiva ou recebem uma ID gerada pelo compilador de marcação na compilação.</span><span class="sxs-lookup"><span data-stu-id="58295-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="58295-136">Os comandos são associados a controles por meio de um nome de comando, mas, ao contrário dos controles, sua funcionalidade real é definida no código em que estão associados a manipuladores de comandos específicos por meio da ID de comando.</span><span class="sxs-lookup"><span data-stu-id="58295-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="58295-137">Na compilação, essa ID é armazenada em um arquivo de cabeçalho de definição de ID que expõe comandos para seus manipuladores de comandos correspondentes no aplicativo host da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="58295-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="58295-138">Cada comando tem um tipo de comando subjacente discriminado na enumeração de [**\_ COMMANDTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .</span><span class="sxs-lookup"><span data-stu-id="58295-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="58295-139">A experiência de comando em ação</span><span class="sxs-lookup"><span data-stu-id="58295-139">The Command Experience In Action</span></span>

<span data-ttu-id="58295-140">Os recursos desse modelo de comando são demonstrados pela barra de ferramentas de acesso rápido da faixa de lista (QAT).</span><span class="sxs-lookup"><span data-stu-id="58295-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="58295-141">O QAT fornece aos usuários finais uma maneira de definir facilmente seus próprios atalhos para praticamente qualquer controle na interface do usuário da faixa de opção.</span><span class="sxs-lookup"><span data-stu-id="58295-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="58295-142">Um atalho é adicionado dinamicamente ao QAT em tempo de execução quando o usuário clica com o botão direito do mouse em um controle da faixa de forma e seleciona **Adicionar à barra de ferramentas de acesso rápido** no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="58295-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="58295-143">A imagem a seguir mostra os comandos **colar** e **colar de** , representados por um controle [**SplitButton**](windowsribbon-element-splitbutton.md) , na faixa de opções do Paint do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="58295-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![imagem do SplitButton de colagem na faixa de faixas do Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="58295-145">A imagem a seguir mostra os mesmos comandos **Paste** e **Paste from** , ainda representados por um controle [**SplitButton**](windowsribbon-element-splitbutton.md) , na faixa de opções qat do Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="58295-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![imagem do SplitButton de colagem no qat do Microsoft Paint.](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="58295-147">Quando um controle é hospedado pelo QAT, a nova instância do controle mantém toda a funcionalidade do controle original sem a necessidade de ouvintes de evento adicionais e manipuladores de comando para dar suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="58295-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="58295-148">Ambos os controles são associados ao mesmo manipulador de comando da faixa de opções por meio de um identificador de comando compartilhado.</span><span class="sxs-lookup"><span data-stu-id="58295-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="58295-149">Dessa forma, a estrutura trata os dois controles como um, independentemente do que é invocado.</span><span class="sxs-lookup"><span data-stu-id="58295-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="58295-150">Os mesmos benefícios são percebidos quando os comandos são incorporados em um [**ContextPopup**](windowsribbon-element-contextpopup.md) em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="58295-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="58295-151">Nesse caso, os manipuladores de comando Paste podem ser usados se o controle [**SplitButton**](windowsribbon-element-splitbutton.md) aparecer na faixa de, qat ou **ContextPopup**.</span><span class="sxs-lookup"><span data-stu-id="58295-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="58295-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58295-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58295-153">Apresentando o Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="58295-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="58295-154">Criando um aplicativo de faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="58295-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="58295-155">Declarando comandos e controles com marcação de faixa de medida</span><span class="sxs-lookup"><span data-stu-id="58295-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 