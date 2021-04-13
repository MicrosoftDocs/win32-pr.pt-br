---
title: Criando um aplicativo de faixa de faixas
description: A estrutura da faixa de opção do Windows é composta por duas plataformas de desenvolvimento diferentes, mas dependentes, uma linguagem de marcação baseada em linguagem XAML (XAML) para declarar controles e seu layout visual, e um conjunto de interfaces com base em C++ Component Object Model (COM) para definir a funcionalidade de comando e os ganchos de aplicativos. Essa divisão de trabalho dentro da arquitetura da estrutura da faixa de Ribbon exige que um desenvolvedor que queira aproveitar os recursos avançados da interface do usuário oferecidos pela estrutura deve criar e descrever a interface do usuário em marcação e, em seguida, usar as interfaces de COM do Framework da faixa de faixas para conectar a estrutura ao aplicativo host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Faixa de-se do Windows, criando aplicativos
- Faixa de faixas, criando aplicativos
- Faixa de mapa do Windows, roteiro
- Faixa de mapa, roteiro
- Faixa de medida do Windows, marcação
- Faixa de, marcação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366437"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="c4464-110">Criando um aplicativo de faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="c4464-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="c4464-111">A estrutura da faixa de opção do Windows é composta por duas plataformas de desenvolvimento diferentes, mas dependentes: uma linguagem de marcação baseada em linguagem XAML (XAML) para declarar controles e seu layout visual, e um conjunto de interfaces baseado em C++ Component Object Model (COM) para definir a funcionalidade de comando e os ganchos de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c4464-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="c4464-112">Essa divisão de trabalho dentro da arquitetura da estrutura da faixa de Ribbon exige que um desenvolvedor que queira aproveitar os recursos avançados da interface do usuário oferecidos pela estrutura deve criar e descrever a interface do usuário em marcação e, em seguida, usar as interfaces de COM do Framework da faixa de faixas para conectar a estrutura ao aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="c4464-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="c4464-113">Roteiro da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="c4464-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="c4464-114">Gravar a marcação</span><span class="sxs-lookup"><span data-stu-id="c4464-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="c4464-115">Compilar a marcação</span><span class="sxs-lookup"><span data-stu-id="c4464-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="c4464-116">Compilar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="c4464-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="c4464-117">Inicializar a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="c4464-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="c4464-118">Vincular a marcação ao aplicativo</span><span class="sxs-lookup"><span data-stu-id="c4464-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="c4464-119">Compilar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="c4464-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="c4464-120">Atualizações e execuções de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c4464-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="c4464-121">Suporte a OLE</span><span class="sxs-lookup"><span data-stu-id="c4464-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="c4464-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4464-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="c4464-123">Roteiro da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="c4464-123">Ribbon Roadmap</span></span>

<span data-ttu-id="c4464-124">Os aspectos visuais de um aplicativo da faixa de faixas, como quais controles são exibidos e onde eles são colocados, são declarados na marcação (consulte [declarando comandos e controles com marcação da faixa de faixas](windowsribbon-schema.md)).</span><span class="sxs-lookup"><span data-stu-id="c4464-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="c4464-125">A lógica do comando do aplicativo, como o que acontece quando um botão é pressionado, é implementada no código.</span><span class="sxs-lookup"><span data-stu-id="c4464-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="c4464-126">O processo de implementar uma faixa de quadro e incorporá-la em um aplicativo do Windows requer quatro tarefas básicas: escreva a marcação, Compile a marcação, grave o código e compile e vincule todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4464-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="c4464-127">O diagrama a seguir ilustra o fluxo de trabalho para uma implementação de faixa de opções típica.</span><span class="sxs-lookup"><span data-stu-id="c4464-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![diagrama mostrando o fluxo de trabalho para uma implementação de faixa de medida típica.](images/overviews/ribbonroadmap.png)

<span data-ttu-id="c4464-129">As seções a seguir descrevem esse processo mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="c4464-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="c4464-130">Gravar a marcação</span><span class="sxs-lookup"><span data-stu-id="c4464-130">Write the Markup</span></span>

<span data-ttu-id="c4464-131">Depois que a interface do usuário da faixa de Ribbon foi projetada, a primeira tarefa para um desenvolvedor de aplicativos é descrever a interface do usuário com a marcação da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="c4464-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4464-132">O arquivo de esquema de marcação de estrutura da faixa de Ribbon, UICC. xsd, é instalado com o Microsoft Windows Software Development Kit (SDK) para Windows 7 e .NET Framework 4,0.</span><span class="sxs-lookup"><span data-stu-id="c4464-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="c4464-133">Usando o caminho de instalação padrão, o arquivo está localizado na pasta% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número da versão \] \\ bin, em que ele pode ser referenciado por muitos editores XML para fornecer dicas e preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="c4464-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="c4464-134">Controles de faixa de opção, comandos de faixa de opção (os elementos independentes de controle que fornecem a funcionalidade base para controles de faixa de forma) e todos os layouts de controle e relações visuais são declarados na marcação.</span><span class="sxs-lookup"><span data-stu-id="c4464-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="c4464-135">A estrutura da marcação da faixa de visão enfatiza a distinção entre controles de faixa de vista e comandos por meio de duas hierarquias de nó primário: uma árvore de [comandos e recursos](windowsribbon-reference-elements-command.md) e uma árvore de [modos de exibição](windowsribbon-reference-elements-view.md) .</span><span class="sxs-lookup"><span data-stu-id="c4464-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="c4464-136">Todos os contêineres e ações que são expostos pela faixa de faixas são declarados na árvore de [comandos e recursos](windowsribbon-reference-elements-command.md) .</span><span class="sxs-lookup"><span data-stu-id="c4464-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="c4464-137">Cada elemento de comando é associado a um conjunto de recursos, conforme exigido pelo design da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c4464-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="c4464-138">Depois de criar os comandos para um aplicativo, você declara os controles na árvore [views](windowsribbon-reference-elements-view.md) e associa cada controle a um comando para expor a funcionalidade do comando.</span><span class="sxs-lookup"><span data-stu-id="c4464-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="c4464-139">A estrutura da faixa de das faixas determina o posicionamento real dos controles com base na hierarquia de controle declarada aqui.</span><span class="sxs-lookup"><span data-stu-id="c4464-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="c4464-140">O exemplo de código a seguir ilustra como declarar um controle de botão, rotulado como sair do aplicativo e associá-lo a um comando de saída.</span><span class="sxs-lookup"><span data-stu-id="c4464-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="c4464-141">Embora seja possível usar qualquer extensão de nome de arquivo para o arquivo de marcação da faixa de faixas, o. xml é a extensão recomendada usada em toda a documentação.</span><span class="sxs-lookup"><span data-stu-id="c4464-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="c4464-142">Compilar a marcação</span><span class="sxs-lookup"><span data-stu-id="c4464-142">Compile the Markup</span></span>

<span data-ttu-id="c4464-143">Depois que o arquivo de marcação da faixa de faixas é criado, ele deve ser compilado em um formato binário pelo compilador de marcação da faixa de forma, UICC (compilador de comando da interface do usuário), incluído no Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c4464-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="c4464-144">Uma referência a esse arquivo binário é passada para o método [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante a inicialização da estrutura da faixa de faixas pelo aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="c4464-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="c4464-145">UICC pode ser executado diretamente de uma janela de linha de comando ou adicionado como uma "etapa de compilação personalizada" no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c4464-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="c4464-146">A imagem a seguir mostra o compilador de marcação UICC na janela shell CMD do SDK do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c4464-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![captura de tela mostrando uicc.exe em uma janela de linha de comando.](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="c4464-148">A imagem a seguir mostra o UICC adicionado como uma etapa de compilação personalizada no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c4464-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![captura de tela mostrando uicc.exe adicionado como uma etapa de compilação personalizada no Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="c4464-150">O UICC gera três arquivos: uma versão binária da marcação (. BML), um cabeçalho de definição de ID (arquivo. h) para expor elementos de marcação ao aplicativo host da faixa de bits e um [script de definição de recurso](../menurc/about-resource-files.md) (arquivo. rc) para vincular a imagem da faixa de bits e recursos de cadeia de caracteres ao aplicativo host no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="c4464-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="c4464-151">Para obter mais detalhes sobre a compilação da marcação da estrutura da faixa de faixas, consulte [compilando marcação da faixa](windowsribbon-intentcl.md)de</span><span class="sxs-lookup"><span data-stu-id="c4464-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="c4464-152">Compilar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="c4464-152">Build the Application</span></span>

<span data-ttu-id="c4464-153">Depois que a interface do usuário preliminar de um aplicativo de faixa de faixas foi projetada e implementada na marcação, o código do aplicativo deve ser escrito que inicializa a estrutura, consome a marcação e associa os comandos declarados na marcação aos manipuladores de comandos apropriados no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4464-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="c4464-154">Como a estrutura da faixa de bits é baseada em COM, é recomendável que os projetos de faixa de bits usem o \_ \_ operador uuidof () para referenciar os GUIDs para as interfaces de estrutura da faixa de referência (IIDs).</span><span class="sxs-lookup"><span data-stu-id="c4464-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="c4464-155">Nesses casos em que não é possível usar o \_ \_ operador uuidof (), como quando um compilador não Microsoft é usado ou o aplicativo host é baseado em C, o IIDs deve ser definido pelo aplicativo, pois eles não estão contidos em UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="c4464-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="c4464-156">Se o IIDs for definido pelo aplicativo, os GUIDs especificados em UIRibbon. idl deverão ser usados.</span><span class="sxs-lookup"><span data-stu-id="c4464-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="c4464-157">O UIRibbon. idl é fornecido como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx) e pode ser encontrado no caminho de instalação padrão de% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ include.</span><span class="sxs-lookup"><span data-stu-id="c4464-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="c4464-158">Inicializar a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="c4464-158">Initialize the Ribbon</span></span>

<span data-ttu-id="c4464-159">O diagrama a seguir ilustra as etapas necessárias para implementar um aplicativo de faixa de opções simples.</span><span class="sxs-lookup"><span data-stu-id="c4464-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![diagrama mostrando as etapas necessárias para implementar uma implementação de faixa de faixas simples.](images/overviews/initializationsteps.png)

<span data-ttu-id="c4464-161">As etapas a seguir descrevem detalhadamente como implementar um aplicativo de faixa de opções simples.</span><span class="sxs-lookup"><span data-stu-id="c4464-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="c4464-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="c4464-162">CoCreateInstance</span></span>

    <span data-ttu-id="c4464-163">O aplicativo chama a função COM CoCreateInstance padrão com a ID de classe da estrutura da faixa de faixas para obter um ponteiro para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="c4464-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="c4464-164">Initialize (HWND, IUIApplication \* )</span><span class="sxs-lookup"><span data-stu-id="c4464-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="c4464-165">O aplicativo chama [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passando dois parâmetros: o identificador para a janela de nível superior que conterá a faixa de faixas e um ponteiro para a implementação de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que permite que a estrutura faça retornos de chamada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4464-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="c4464-166">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="c4464-166">\[!Important\]</span></span>  
    > <span data-ttu-id="c4464-167">A estrutura da faixa de faixas é inicializada como um STA (single-threaded apartment).</span><span class="sxs-lookup"><span data-stu-id="c4464-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="c4464-168">LoadUI (instância, resourceName)</span><span class="sxs-lookup"><span data-stu-id="c4464-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="c4464-169">O aplicativo chama [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para associar o recurso de marcação.</span><span class="sxs-lookup"><span data-stu-id="c4464-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="c4464-170">O primeiro parâmetro dessa função é um identificador para a instância do aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="c4464-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="c4464-171">O segundo parâmetro é o nome do recurso de marcação binária que foi compilado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c4464-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="c4464-172">Ao passar a marcação binária para a estrutura da faixa de faixas, o aplicativo sinaliza o que a estrutura da faixa de faixas deve ser e como os controles devem ser organizados.</span><span class="sxs-lookup"><span data-stu-id="c4464-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="c4464-173">Ele também fornece a estrutura com um manifesto de comandos para expor (como colar, recortar, localizar), que são usados pela estrutura quando ele faz retornos de chamada relacionados a comandos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c4464-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="c4464-174">Retornos de chamada [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)</span><span class="sxs-lookup"><span data-stu-id="c4464-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="c4464-175">Após a conclusão das etapas 1 a 3, a estrutura da faixa de faixas sabe quais comandos serão expostos na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="c4464-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="c4464-176">No entanto, a estrutura ainda precisa de duas coisas antes que a faixa de opções seja totalmente funcional: uma maneira de informar ao aplicativo quando comandos são executados e uma maneira de obter recursos de comando, ou propriedades, em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c4464-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="c4464-177">Por exemplo, se uma caixa de combinação for exibida na interface do usuário, a estrutura precisará solicitar os itens com os quais preencher a caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="c4464-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="c4464-178">Essas duas partes de funcionalidade são manipuladas por meio da interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="c4464-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="c4464-179">Especificamente, para cada comando declarado na marcação binária (consulte a etapa 3 acima), a estrutura chama [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) para solicitar ao aplicativo um objeto **IUICommandHandler** para esse comando</span><span class="sxs-lookup"><span data-stu-id="c4464-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="c4464-180">A interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permite que um manipulador de comando seja associado a um ou mais comandos.</span><span class="sxs-lookup"><span data-stu-id="c4464-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="c4464-181">No mínimo, o aplicativo é necessário para implementar stubs de métodos [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que retornam E \_ NOTIMPL, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4464-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="c4464-182">Vincular a marcação ao aplicativo</span><span class="sxs-lookup"><span data-stu-id="c4464-182">Link the Markup to the Application</span></span>

<span data-ttu-id="c4464-183">Neste ponto, os arquivos de recursos de marcação devem ser vinculados ao aplicativo host, incluindo uma referência ao arquivo de definição de recurso de marcação (que contém uma referência ao arquivo de cabeçalho de marcação) no arquivo de recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4464-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="c4464-184">Por exemplo, um aplicativo chamado RibbonApp com um arquivo de recurso chamado ribbonUI. rc requer a seguinte linha no arquivo RibbonApp. rc.</span><span class="sxs-lookup"><span data-stu-id="c4464-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="c4464-185">Dependendo do compilador e do vinculador que está sendo usado, o script de definição de recurso também pode exigir compilação antes que o aplicativo da faixa de faixas possa ser compilado.</span><span class="sxs-lookup"><span data-stu-id="c4464-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="c4464-186">A ferramenta de linha de comando do [compilador de recursos (RC)](../menurc/using-rc-the-rc-command-line-.md) fornecida com Microsoft Visual Studio e a SDK do Windows pode ser usada para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="c4464-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="c4464-187">Compilar o aplicativo</span><span class="sxs-lookup"><span data-stu-id="c4464-187">Compile the Application</span></span>

<span data-ttu-id="c4464-188">Depois que o aplicativo da faixa de faixas é compilado, ele pode ser executado e a interface do usuário é testada.</span><span class="sxs-lookup"><span data-stu-id="c4464-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="c4464-189">Se a interface do usuário exigir ajuste e não houver nenhuma alteração em nenhum manipulador de comando associado no código do aplicativo principal, revise o arquivo de origem da marcação, recompile a marcação com UICC.exe e vincule os novos arquivos de recurso de marcação.</span><span class="sxs-lookup"><span data-stu-id="c4464-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="c4464-190">Quando o aplicativo é reiniciado, a interface do usuário modificada é exibida.</span><span class="sxs-lookup"><span data-stu-id="c4464-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="c4464-191">Tudo isso é possível sem tocar no código do aplicativo principal – uma melhoria significativa em relação ao desenvolvimento e à distribuição de aplicativos padrão.</span><span class="sxs-lookup"><span data-stu-id="c4464-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="c4464-192">Atualizações e execuções de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="c4464-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="c4464-193">A estrutura de comunicação de tempo de execução da estrutura da faixa de opção baseia-se em um modelo de chamada push e pull, ou um chamador bidirecional.</span><span class="sxs-lookup"><span data-stu-id="c4464-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="c4464-194">Esse modelo permite que a estrutura informe o aplicativo quando um comando é executado e permite que a estrutura e o aplicativo consultem, atualizem e invalidam valores de propriedade e recursos de faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="c4464-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="c4464-195">Essa funcionalidade é fornecida por meio de várias interfaces e métodos.</span><span class="sxs-lookup"><span data-stu-id="c4464-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="c4464-196">A estrutura extrai informações de propriedade atualizadas do aplicativo da faixa de faixas por meio do método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c4464-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="c4464-197">Uma ID de comando e uma chave de propriedade, que identifica a propriedade de comando a ser atualizada, são passadas para o método que, em seguida, retorna ou envia um valor para essa chave de propriedade para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="c4464-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="c4464-198">A estrutura chama [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando um comando é executado, identificando a ID de comando e o tipo de execução que ocorreu ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span><span class="sxs-lookup"><span data-stu-id="c4464-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="c4464-199">É aí que o aplicativo especifica a lógica de execução para um comando.</span><span class="sxs-lookup"><span data-stu-id="c4464-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="c4464-200">O diagrama a seguir ilustra a comunicação em tempo de execução para a execução do comando entre a estrutura e o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4464-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![diagrama que mostra um exemplo da comunicação de tempo de execução entre a estrutura da faixa de bits e um aplicativo host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="c4464-202">A implementação das funções [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) não é necessária para exibir inicialmente uma faixa de faixas em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c4464-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="c4464-203">No entanto, esses métodos são necessários para garantir que o aplicativo funcione corretamente quando comandos são executados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c4464-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="c4464-204">Suporte a OLE</span><span class="sxs-lookup"><span data-stu-id="c4464-204">OLE Support</span></span>

<span data-ttu-id="c4464-205">Um aplicativo de faixa de faixas pode ser configurado como um servidor OLE para dar suporte à ativação de OLE fora do local.</span><span class="sxs-lookup"><span data-stu-id="c4464-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="c4464-206">Os objetos criados em um aplicativo de servidor OLE mantêm sua associação com o aplicativo de servidor quando inseridos (colados ou posicionados) em um aplicativo cliente OLE (ou contêiner).</span><span class="sxs-lookup"><span data-stu-id="c4464-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="c4464-207">Em ativação de OLE fora do local, clicar duas vezes no objeto no aplicativo cliente abre uma instância dedicada do aplicativo de servidor e carrega o objeto para edição.</span><span class="sxs-lookup"><span data-stu-id="c4464-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="c4464-208">Quando o aplicativo do servidor é fechado, todas as alterações feitas no objeto são refletidas no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c4464-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="c4464-209">A estrutura da faixa de bits não dá suporte à ativação de OLE in-loco.</span><span class="sxs-lookup"><span data-stu-id="c4464-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="c4464-210">Os objetos criados em um servidor OLE baseado em faixa de bits não podem ser editados de dentro do aplicativo cliente OLE.</span><span class="sxs-lookup"><span data-stu-id="c4464-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="c4464-211">Uma instância dedicada externa do aplicativo de servidor é necessária.</span><span class="sxs-lookup"><span data-stu-id="c4464-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="c4464-212">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c4464-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4464-213">Declarando comandos e controles com marcação de faixa de medida</span><span class="sxs-lookup"><span data-stu-id="c4464-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="c4464-214">Diretrizes de experiência do usuário da faixa de das</span><span class="sxs-lookup"><span data-stu-id="c4464-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="c4464-215">Processo de design da faixa de das</span><span class="sxs-lookup"><span data-stu-id="c4464-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




