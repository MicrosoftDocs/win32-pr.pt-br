---
description: Este tutorial demonstra como usar um aplicativo multilíngue e torná-lo preparado para o mundo. Esse aplicativo está na forma de uma solução completa criada em Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Adicionando suporte à interface do usuário multilíngue a um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836852"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="fdf7a-104">Adicionando suporte à interface do usuário multilíngue a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="fdf7a-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="fdf7a-105">Este tutorial demonstra como usar um aplicativo multilíngue e torná-lo preparado para o mundo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="fdf7a-106">Esse aplicativo está na forma de uma solução completa criada em Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="fdf7a-107">Visão geral</span><span class="sxs-lookup"><span data-stu-id="fdf7a-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="fdf7a-108">A ideia por trás do MUI de Hello</span><span class="sxs-lookup"><span data-stu-id="fdf7a-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="fdf7a-109">Configurando a solução de Hello MUI</span><span class="sxs-lookup"><span data-stu-id="fdf7a-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="fdf7a-110">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="fdf7a-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="fdf7a-111">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fdf7a-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="fdf7a-112">Etapa 0: criando o MUI de Hello embutido em código</span><span class="sxs-lookup"><span data-stu-id="fdf7a-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="fdf7a-113">Etapa 1: Implementando o módulo de recurso básico</span><span class="sxs-lookup"><span data-stu-id="fdf7a-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="fdf7a-114">Etapa 2: criando o módulo de recurso básico</span><span class="sxs-lookup"><span data-stu-id="fdf7a-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="fdf7a-115">Dividindo os vários módulos de recursos de linguagem: uma visão geral</span><span class="sxs-lookup"><span data-stu-id="fdf7a-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="fdf7a-116">Dividindo os vários módulos de recursos de linguagem: criando os arquivos</span><span class="sxs-lookup"><span data-stu-id="fdf7a-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="fdf7a-117">Etapa 3: Criando um Resource-Savvy "Olá, MUI"</span><span class="sxs-lookup"><span data-stu-id="fdf7a-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="fdf7a-118">Etapa 4: Globalizando "Olá, MUI"</span><span class="sxs-lookup"><span data-stu-id="fdf7a-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="fdf7a-119">Etapa 5: Personalizando "Olá, MUI"</span><span class="sxs-lookup"><span data-stu-id="fdf7a-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="fdf7a-120">Considerações adicionais sobre o MUI</span><span class="sxs-lookup"><span data-stu-id="fdf7a-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="fdf7a-121">Suporte para aplicativos de console</span><span class="sxs-lookup"><span data-stu-id="fdf7a-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="fdf7a-122">Determinação de idiomas para dar suporte em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="fdf7a-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="fdf7a-123">Suporte a scripts complexos em versões anteriores ao Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdf7a-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="fdf7a-124">Resumo</span><span class="sxs-lookup"><span data-stu-id="fdf7a-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="fdf7a-125">Visão geral</span><span class="sxs-lookup"><span data-stu-id="fdf7a-125">Overview</span></span>

<span data-ttu-id="fdf7a-126">A partir do Windows Vista, o próprio sistema operacional Windows foi criado desde o início para ser uma plataforma multilíngue, com suporte adicional que permite criar aplicativos multilíngues que usam o modelo de recurso MUI do Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="fdf7a-127">Este tutorial ilustra esse novo suporte para aplicativos multilíngües ao abranger os seguintes aspectos:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="fdf7a-128">O usa o suporte aprimorado à plataforma MUI para permitir facilmente aplicativos multilíngües.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="fdf7a-129">Estende os aplicativos multilíngues para serem executados em versões do Windows anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="fdf7a-130">Aborda as considerações adicionais envolvidas no desenvolvimento de aplicativos multilíngües especializados, como aplicativos de console.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="fdf7a-131">Esses links ajudam a fornecer uma rápida atualização sobre os conceitos sobre internacionalização e o MUI:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="fdf7a-132">[Visão geral rápida da internacionalização](understanding-internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="fdf7a-133">[Conceitos do MUI](understanding-mui.md).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="fdf7a-134">[Usando o MUI para desenvolver aplicativos Win32](using-multilingual-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="fdf7a-135">A ideia por trás do MUI de Hello</span><span class="sxs-lookup"><span data-stu-id="fdf7a-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="fdf7a-136">Você provavelmente está familiarizado com o aplicativo Olá, Mundo clássico, que ilustra os conceitos básicos de programação.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="fdf7a-137">Este tutorial usa uma abordagem semelhante para ilustrar como usar o modelo de recurso MUI para atualizar um aplicativo multilíngue para criar uma versão multilíngue chamada Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="fdf7a-138">As tarefas neste tutorial são descritas em etapas detalhadas devido à precisão com a qual essas atividades devem ser executadas e a necessidade de explicar os detalhes para os desenvolvedores que têm pouca experiência com essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="fdf7a-139">Configurando a solução de Hello MUI</span><span class="sxs-lookup"><span data-stu-id="fdf7a-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="fdf7a-140">Estas etapas descrevem como se preparar para criar a solução de Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="fdf7a-141">Requisitos de plataforma</span><span class="sxs-lookup"><span data-stu-id="fdf7a-141">Platform Requirements</span></span>

<span data-ttu-id="fdf7a-142">Você deve compilar os exemplos de código neste tutorial usando o SDK (Software Development Kit) do Windows para o Windows 7 e o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="fdf7a-143">O SDK do Windows 7 será instalado no Windows XP, no Windows Vista e no Windows 7, e a solução de exemplo pode ser criada em qualquer uma dessas versões de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="fdf7a-144">Todos os exemplos de código neste tutorial foram projetados para serem executados em versões x86 e x64 do Windows XP, Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="fdf7a-145">Partes específicas que não funcionarão no Windows XP são chamadas de quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="fdf7a-146">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fdf7a-146">Prerequisites</span></span>

1.  <span data-ttu-id="fdf7a-147">Instale o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="fdf7a-148">Para obter mais informações, consulte o [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="fdf7a-149">Instale o SDK do Windows para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="fdf7a-150">Você pode instalá-lo na página SDK do Windows do [centro de desenvolvedores do Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="fdf7a-151">O SDK inclui utilitários para desenvolver aplicativos para versões do sistema operacional a partir do Windows XP por meio do mais recente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="fdf7a-152">Se você não estiver instalando o pacote no local padrão, ou se não estiver instalando na unidade do sistema, que geralmente é a unidade C, anote o caminho de instalação.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="fdf7a-153">Configure os parâmetros de linha de comando do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="fdf7a-154">Abra uma janela de comando do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="fdf7a-155">Digite o **caminho do conjunto**.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="fdf7a-156">Confirme se a variável de caminho inclui o caminho da pasta bin do SDK do Windows 7:... Compartimento do \\ Windows \\ v 7.0 do Microsoft SDKs \\</span><span class="sxs-lookup"><span data-stu-id="fdf7a-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="fdf7a-157">Instale o pacote complementar de APIs de nível inferior do Microsoft NLS.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="fdf7a-158">No contexto deste tutorial, esse pacote será necessário apenas se você estiver personalizando o aplicativo para ser executado em versões do Windows anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="fdf7a-159">Consulte [Step 5: Personalizando Hello MUI](#step-5-customizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="fdf7a-160">Baixe e instale o pacote de seu [site de download](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="fdf7a-161">Assim como ocorre com o SDK do Windows, se você não estiver instalando o pacote no local padrão ou se não estiver instalando na unidade do sistema, que geralmente é a unidade C, anote o caminho de instalação.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="fdf7a-162">Se sua plataforma de desenvolvimento for o Windows XP ou o Windows Server 2003, confirme se o Nlsdl.dll está instalado e registrado corretamente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="fdf7a-163">Navegue até a pasta "Redist" no local do caminho de instalação.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="fdf7a-164">Execute o nlsdl redistribuível apropriado \* . exe, como nlsdl.x86.exe.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="fdf7a-165">Esta etapa instala e registra Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="fdf7a-166">Se você desenvolver um aplicativo que usa o MUI e que deve ser executado em versões do Windows anteriores ao Windows Vista, Nlsdl.dll deverá estar presente na plataforma Windows de destino.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="fdf7a-167">Na maioria dos casos, isso significa que o aplicativo precisa executar e instalar o instalador nlsdl redistribuível (e não meramente copiar Nlsdl.dll si mesmo).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="fdf7a-168">Etapa 0: criando o MUI de Hello embutido em código</span><span class="sxs-lookup"><span data-stu-id="fdf7a-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="fdf7a-169">Este tutorial começa com a versão multilíngue do aplicativo Hello MUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="fdf7a-170">O aplicativo assume o uso da linguagem de programação C++, cadeias de caracteres largos e a função [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) para saída.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="fdf7a-171">Comece criando o \_ aplicativo GuiStep 0 inicial, bem como a solução HelloMUI, que contém todos os aplicativos deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="fdf7a-172">No Visual Studio 2008, crie um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="fdf7a-173">Use as seguintes configurações e valores:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="fdf7a-174">Tipo de projeto: em Visual C++ selecione Win32 e, em seguida, em modelos instalados do Visual Studio, selecione projeto Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="fdf7a-175">Nome: GuiStep \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="fdf7a-176">Local: *ProjectRootDirectory* (as etapas posteriores fazem referência a esse diretório).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="fdf7a-177">Nome da solução: HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="fdf7a-178">Selecione criar diretório para solução.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="fdf7a-179">No assistente de aplicativo Win32, selecione o tipo de aplicativo padrão: aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="fdf7a-180">Configurar o modelo de Threading do projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="fdf7a-181">Na Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep \_ 0 e selecione Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="fdf7a-182">Na caixa de diálogo páginas de propriedades do projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="fdf7a-183">Na lista suspensa superior esquerda, defina configuração para todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="fdf7a-184">Em Propriedades de configuração, expanda C/C++, selecione geração de código e defina biblioteca de tempo de execução: depuração multi-threaded (/MTd).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="fdf7a-185">Substitua o conteúdo de GuiStep \_ 0. cpp pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  <span data-ttu-id="fdf7a-186">Crie e execute o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-186">Build and run the application.</span></span>

<span data-ttu-id="fdf7a-187">O código-fonte direto acima faz a simples opção de design de codificação embutida, ou inserção, toda a saída que o usuário verá — nesse caso, o texto "Olá, MUI".</span><span class="sxs-lookup"><span data-stu-id="fdf7a-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="fdf7a-188">Essa opção limita o utilitário do aplicativo para usuários que não reconhecem a palavra em inglês "Olá".</span><span class="sxs-lookup"><span data-stu-id="fdf7a-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="fdf7a-189">Como o MUI é um acrônimo em inglês baseado em tecnologia, presume-se que a cadeia de caracteres permaneça "MUI" para todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="fdf7a-190">Etapa 1: Implementando o módulo de recurso básico</span><span class="sxs-lookup"><span data-stu-id="fdf7a-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="fdf7a-191">O Microsoft Win32 expunha muito o recurso para que os desenvolvedores de aplicativos separem seus dados de recursos de interface do usuário do código-fonte do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="fdf7a-192">Essa separação vem na forma do modelo de recurso do Win32, em que cadeias de caracteres, bitmaps, ícones, mensagens e outros itens normalmente exibidos para um usuário são empacotados em uma seção distinta do executável, separados do código executável.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="fdf7a-193">Para ilustrar essa separação entre o código executável e o empacotamento de dados de recursos, nesta etapa o tutorial coloca a cadeia de caracteres "Olá" embutida em código (o recurso "en-US") na seção de recursos de um módulo DLL no \_ projeto HelloModule en \_ US.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="fdf7a-194">Essa DLL Win32 também poderia conter a funcionalidade executável do tipo de biblioteca (como qualquer outra DLL).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="fdf7a-195">Mas para ajudar a se concentrar nos aspectos relacionados a recursos do Win32, deixamos o código DLL de tempo de execução fragmentado em DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="fdf7a-196">As seções subsequentes deste tutorial fazem uso dos dados do recurso HelloModule que estão sendo criados aqui e também apresentam o código de tempo de execução apropriado.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="fdf7a-197">Para construir um módulo de recurso do Win32, comece criando uma DLL com um DllMain fragmentado out:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="fdf7a-198">Adicione um novo projeto à solução HelloMUI:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="fdf7a-199">No menu arquivo, selecione Adicionar e novo projeto.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="fdf7a-200">Tipo de projeto: projeto Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="fdf7a-201">Nome: HelloModule \_ en \_ US.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="fdf7a-202">Local: *ProjectRootDirectory* \\ HelloMUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="fdf7a-203">No assistente de aplicativo Win32, selecione tipo de aplicativo: DLL.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="fdf7a-204">Configure o modelo de Threading deste projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="fdf7a-205">Na Gerenciador de Soluções, clique com o botão direito do mouse no projeto HelloModule \_ en \_ US e selecione Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="fdf7a-206">Na caixa de diálogo páginas de propriedades do projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="fdf7a-207">Na lista suspensa superior esquerda, defina configuração para todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="fdf7a-208">Em Propriedades de configuração, expanda C/C++, selecione geração de código e defina biblioteca de tempo de execução: depuração multi-threaded (/MTd).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="fdf7a-209">Examine DllMain. cpp.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="fdf7a-210">(Talvez você queira adicionar a referência não referenciada \_ Macros de parâmetro para o código gerado, como temos aqui, para permitir que ele seja compilado no nível de aviso 4.)</span><span class="sxs-lookup"><span data-stu-id="fdf7a-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  <span data-ttu-id="fdf7a-211">Adicione um arquivo de definição de recurso HelloModule. rc ao projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="fdf7a-212">No projeto HelloModule \_ \_ , clique com o botão direito do mouse na pasta arquivos de recursos e selecione Adicionar e, em seguida, selecione novo item.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="fdf7a-213">Na caixa de diálogo Adicionar novo item, escolha o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="fdf7a-214">Categorias: em Visual C++ selecione recurso e, em seguida, em "modelos instalados do Visual Studio", selecione o arquivo de recurso (. rc).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="fdf7a-215">Nome: HelloModule.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="fdf7a-216">Local: aceite o padrão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="fdf7a-217">Clique em Adicionar.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-217">Click Add.</span></span>

    3.  <span data-ttu-id="fdf7a-218">Especifique que o novo arquivo HelloModule. rc deve ser salvo como Unicode:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="fdf7a-219">Na Gerenciador de Soluções, clique com o botão direito do mouse em HelloModule. rc e selecione Exibir código.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="fdf7a-220">Se você vir uma mensagem informando que o arquivo já está aberto e perguntará se deseja fechá-lo, clique em Sim.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="fdf7a-221">Com o arquivo exibido como texto, faça o arquivo de seleção de menu e as opções avançadas de salvamento.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="fdf7a-222">Em codificação, especifique Unicode-CodePage 1200.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="fdf7a-223">Clique em OK.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-223">Click OK.</span></span>
        6.  <span data-ttu-id="fdf7a-224">Salve e feche o HelloModule. rc.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="fdf7a-225">Adicione uma tabela de cadeia de caracteres que contém a cadeia de caracteres "Olá":</span><span class="sxs-lookup"><span data-stu-id="fdf7a-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="fdf7a-226">Na Modo de Exibição de Recursos, clique com o botão direito do mouse em HelloModule. rc e selecione Adicionar recurso.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="fdf7a-227">Selecione a tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-227">Select String Table.</span></span>
        3.  <span data-ttu-id="fdf7a-228">Clique em Novo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-228">Click New.</span></span>
        4.  <span data-ttu-id="fdf7a-229">Adicione uma cadeia de caracteres à tabela de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="fdf7a-230">ID: Olá \_ MUI \_ Str \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="fdf7a-231">Valor: 0.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-231">Value: 0.</span></span>
            3.  <span data-ttu-id="fdf7a-232">Legenda: Olá.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-232">Caption: Hello.</span></span>

        <span data-ttu-id="fdf7a-233">Se você exibir HelloModule. rc como texto agora, verá várias partes do código-fonte específico do recurso.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="fdf7a-234">O maior interesse é a seção que descreve a cadeia de caracteres "Olá":</span><span class="sxs-lookup"><span data-stu-id="fdf7a-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        <span data-ttu-id="fdf7a-235">Essa cadeia de caracteres "Olá" é o recurso que precisa ser localizado (ou seja, traduzido) em todas as linguagens que o aplicativo espera oferecer suporte.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="fdf7a-236">Por exemplo, o HelloModule \_ ta \_ no projeto (que você criará na próxima etapa) conterá sua própria versão localizada de HelloModule. rc para "ta-in":</span><span class="sxs-lookup"><span data-stu-id="fdf7a-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  <span data-ttu-id="fdf7a-237">Crie o \_ projeto HelloModule en \_ US para ter certeza de que não há erros.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="fdf7a-238">Crie mais seis projetos na solução HelloMUI (ou quantos quiser) para criar mais seis DLLs de recurso para idiomas adicionais.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="fdf7a-239">Use os valores nesta tabela:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-239">Use the values in this table:</span></span>

    | <span data-ttu-id="fdf7a-240">Nome do projeto</span><span class="sxs-lookup"><span data-stu-id="fdf7a-240">Project name</span></span>        | <span data-ttu-id="fdf7a-241">Nome do arquivo. rc</span><span class="sxs-lookup"><span data-stu-id="fdf7a-241">Name of .rc file</span></span> | <span data-ttu-id="fdf7a-242">ID da Cadeia de Caracteres</span><span class="sxs-lookup"><span data-stu-id="fdf7a-242">String ID</span></span>          | <span data-ttu-id="fdf7a-243">Valor da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="fdf7a-243">String value</span></span> | <span data-ttu-id="fdf7a-244">Legenda da cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="fdf7a-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="fdf7a-245">HelloModule \_ de \_ de</span><span class="sxs-lookup"><span data-stu-id="fdf7a-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="fdf7a-246">HelloModule</span><span class="sxs-lookup"><span data-stu-id="fdf7a-246">HelloModule</span></span>      | <span data-ttu-id="fdf7a-247">Olá \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="fdf7a-248">0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-248">0</span></span>            | <span data-ttu-id="fdf7a-249">Hallo</span><span class="sxs-lookup"><span data-stu-id="fdf7a-249">Hallo</span></span>          |
    | <span data-ttu-id="fdf7a-250">HelloModule \_ es \_ es</span><span class="sxs-lookup"><span data-stu-id="fdf7a-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="fdf7a-251">HelloModule</span><span class="sxs-lookup"><span data-stu-id="fdf7a-251">HelloModule</span></span>      | <span data-ttu-id="fdf7a-252">Olá \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="fdf7a-253">0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-253">0</span></span>            | <span data-ttu-id="fdf7a-254">Hola</span><span class="sxs-lookup"><span data-stu-id="fdf7a-254">Hola</span></span>           |
    | <span data-ttu-id="fdf7a-255">HelloModule \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="fdf7a-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="fdf7a-256">HelloModule</span><span class="sxs-lookup"><span data-stu-id="fdf7a-256">HelloModule</span></span>      | <span data-ttu-id="fdf7a-257">Olá \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="fdf7a-258">0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-258">0</span></span>            | <span data-ttu-id="fdf7a-259">Bonjour</span><span class="sxs-lookup"><span data-stu-id="fdf7a-259">Bonjour</span></span>        |
    | <span data-ttu-id="fdf7a-260">HelloModule \_ Hi \_</span><span class="sxs-lookup"><span data-stu-id="fdf7a-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="fdf7a-261">HelloModule</span><span class="sxs-lookup"><span data-stu-id="fdf7a-261">HelloModule</span></span>      | <span data-ttu-id="fdf7a-262">Olá \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="fdf7a-263">0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-263">0</span></span>            | <span data-ttu-id="fdf7a-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="fdf7a-264">नमस्</span></span>           |
    | <span data-ttu-id="fdf7a-265">HelloModule \_ ru \_ ru</span><span class="sxs-lookup"><span data-stu-id="fdf7a-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="fdf7a-266">HelloModule</span><span class="sxs-lookup"><span data-stu-id="fdf7a-266">HelloModule</span></span>      | <span data-ttu-id="fdf7a-267">Olá \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="fdf7a-268">0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-268">0</span></span>            | <span data-ttu-id="fdf7a-269">Здравствуйте</span><span class="sxs-lookup"><span data-stu-id="fdf7a-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="fdf7a-270">HelloModule \_ ta \_</span><span class="sxs-lookup"><span data-stu-id="fdf7a-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="fdf7a-271">HelloModule</span><span class="sxs-lookup"><span data-stu-id="fdf7a-271">HelloModule</span></span>      | <span data-ttu-id="fdf7a-272">Olá \_ MUI \_ Str \_ 0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="fdf7a-273">0</span><span class="sxs-lookup"><span data-stu-id="fdf7a-273">0</span></span>            | <span data-ttu-id="fdf7a-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="fdf7a-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="fdf7a-275">Para obter mais informações sobre a estrutura e a sintaxe do arquivo. rc, consulte [About Resource files](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="fdf7a-276">Etapa 2: criando o módulo de recurso básico</span><span class="sxs-lookup"><span data-stu-id="fdf7a-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="fdf7a-277">Usando modelos de recursos anteriores, a criação de qualquer um dos sete projetos HelloModule resultaria em sete DLLs separadas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="fdf7a-278">Cada DLL contém uma seção de recursos com uma única cadeia de caracteres localizada no idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="fdf7a-279">Embora apropriado para o modelo de recurso do Win32 histórico, esse design não aproveita o MUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="fdf7a-280">No SDK do Windows Vista e posterior, o MUI fornece a capacidade de dividir os executáveis no código-fonte e nos módulos de conteúdo localizáveis.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="fdf7a-281">Com a personalização adicional que é abordada posteriormente na etapa 5, os aplicativos podem ser habilitados para suporte multilíngue para execução em versões anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="fdf7a-282">Os principais mecanismos disponíveis para dividir os recursos do código executável, começando com o Windows Vista, são:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="fdf7a-283">Usando rc.exe (o compilador RC) com opções específicas ou</span><span class="sxs-lookup"><span data-stu-id="fdf7a-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="fdf7a-284">Usando uma ferramenta de divisão de estilo de pós-compilação chamada muirct.exe.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="fdf7a-285">Consulte [utilitários de recursos](resource-utilities.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="fdf7a-286">Para simplificar, este tutorial usa muirct.exe para dividir o executável "Hello MUI".</span><span class="sxs-lookup"><span data-stu-id="fdf7a-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="fdf7a-287">Dividindo os vários módulos de recursos de linguagem: uma visão geral</span><span class="sxs-lookup"><span data-stu-id="fdf7a-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="fdf7a-288">Um processo de várias partes é envolvido na divisão de DLLs em um executável HelloModule.dll, além de um HelloModule.dll. mui para cada um dos sete idiomas com suporte neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="fdf7a-289">Esta visão geral descreve as etapas necessárias; a próxima seção apresenta um arquivo de comando que executa essas etapas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="fdf7a-290">Primeiro, divida o módulo HelloModule.dll somente em inglês usando o comando:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="fdf7a-291">A linha de comando acima usa o arquivo de configuração DoReverseMuiLoc. rcconfig.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="fdf7a-292">Esse tipo de arquivo de configuração normalmente é usado pelo muirct.exe para dividir os recursos entre a DLL do LN (linguagem neutra) e os arquivos. mui dependentes do idioma.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="fdf7a-293">Nesse caso, o arquivo XML DoReverseMuiLoc. rcconfig (listado na próxima seção) indica muitos tipos de recursos, mas todos eles se encaixam na categoria de arquivo "localizedResources" ou. mui, e não há recursos na categoria idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="fdf7a-294">Para obter mais informações sobre como preparar um arquivo de configuração de recurso, consulte [preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="fdf7a-295">Além de criar um arquivo HelloModule.dll. mui que contém a cadeia de caracteres em inglês "Olá", muirct.exe também insere um recurso MUI no módulo HelloModule.dll durante a divisão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="fdf7a-296">Para carregar corretamente em tempo de execução os recursos apropriados dos módulos HelloModule.dll. mui específicos do idioma, cada arquivo. mui deve ter suas somas de verificação fixas para corresponder às somas de verificação no módulo LN da linguagem de linha de base neutro.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="fdf7a-297">Isso é feito por um comando como:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="fdf7a-298">Da mesma forma, muirct.exe é invocado para criar um arquivo HelloModule.dll. mui para cada um dos outros idiomas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="fdf7a-299">No entanto, nesses casos, a DLL neutra de idioma é descartada, pois apenas a primeira criada será necessária.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="fdf7a-300">Os comandos que processam os recursos em espanhol e francês têm a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="fdf7a-301">Uma das coisas mais importantes a serem observadas no muirct.exe linhas de comando acima é que o sinalizador-x é usado para especificar uma ID de idioma de destino.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="fdf7a-302">O valor fornecido para muirct.exe é diferente para cada módulo de HelloModule.dll específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="fdf7a-303">Esse valor de idioma é central e é usado pelo muirct.exe para marcar apropriadamente o arquivo. mui durante a divisão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="fdf7a-304">Um valor incorreto produz falhas de carregamento de recursos para esse arquivo. mui específico em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="fdf7a-305">Consulte [constantes e cadeias de caracteres de identificador de linguagem](language-identifier-constants-and-strings.md) para obter mais detalhes sobre como mapear o nome do idioma para LCID.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="fdf7a-306">Cada arquivo Split. mui acaba sendo colocado em um diretório correspondente ao nome do idioma, imediatamente abaixo do diretório no qual o HelloModule.dll neutro de idioma residirá.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="fdf7a-307">Para obter mais informações sobre o posicionamento do arquivo. mui, consulte [implantação de aplicativos](application-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="fdf7a-308">Dividindo os vários módulos de recursos de linguagem: criando os arquivos</span><span class="sxs-lookup"><span data-stu-id="fdf7a-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="fdf7a-309">Para este tutorial, você cria um arquivo de comando que contém os comandos para dividir as várias DLLs e a chama manualmente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="fdf7a-310">Observe que, no trabalho de desenvolvimento real, você pode reduzir o potencial de erros de compilação, incluindo esses comandos como eventos de pré-compilação ou pós-compilação na solução HelloMUI, mas isso está além do escopo deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="fdf7a-311">Crie os arquivos para a compilação de depuração:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="fdf7a-312">Crie um arquivo de comando DoReverseMuiLoc. cmd contendo os seguintes comandos:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  <span data-ttu-id="fdf7a-313">Crie um arquivo XML DoReverseMuiLoc. rcconfig que contenha as seguintes linhas:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  <span data-ttu-id="fdf7a-314">Copie DoReverseMuiLoc. cmd e DoReverseMuiLoc. rcconfig para *ProjectRootDirectory* \\ HelloMUI \\ debug.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="fdf7a-315">Abra o prompt de comando do Visual Studio 2008 e navegue até o diretório de depuração.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="fdf7a-316">Execute DoReverseMuiLoc. cmd.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="fdf7a-317">Ao criar uma compilação de versão, você copia os mesmos arquivos DoReverseMuiLoc. cmd e DoReverseMuiLoc. rcconfig para o diretório de liberação e executa o arquivo de comando lá.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="fdf7a-318">Etapa 3: Criando um Resource-Savvy "Olá, MUI"</span><span class="sxs-lookup"><span data-stu-id="fdf7a-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="fdf7a-319">Com a criação do exemplo inicial embutido em código \_0.exe GuiStep acima, você pode estender o alcance do aplicativo para vários usuários de idioma, optando por incorporar o modelo de recurso do Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="fdf7a-320">O novo código de tempo de execução apresentado nesta etapa inclui a lógica de carregamento de módulo ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) e de recuperação de cadeia de caracteres ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="fdf7a-321">Adicione um novo projeto à solução HelloMUI (usando o menu seleção arquivo, adicionar e novo projeto) com as seguintes configurações e valores:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="fdf7a-322">Tipo de projeto: projeto Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="fdf7a-323">Nome: GuiStep \_ 1.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="fdf7a-324">Local: aceite o padrão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="fdf7a-325">No assistente de aplicativo Win32, selecione o tipo de aplicativo padrão: aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="fdf7a-326">Defina este projeto para ser executado no Visual Studio e configure seu modelo de Threading:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="fdf7a-327">Na Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep \_ 1 e selecione Definir como projeto de inicialização.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="fdf7a-328">Clique com o botão direito do mouse novamente e selecione Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="fdf7a-329">Na caixa de diálogo páginas de propriedades do projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="fdf7a-330">Na lista suspensa superior esquerda, defina configuração para todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="fdf7a-331">Em Propriedades de configuração, expanda C/C++, selecione geração de código e defina biblioteca de tempo de execução: depuração multi-threaded (/MTd).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="fdf7a-332">Substitua o conteúdo de GuiStep \_ 1. cpp pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  <span data-ttu-id="fdf7a-333">Crie e execute o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-333">Build and run the application.</span></span> <span data-ttu-id="fdf7a-334">A saída será exibida no idioma definido atualmente como o idioma de exibição do computador (desde que seja um dos sete idiomas que criamos).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="fdf7a-335">Etapa 4: Globalizando "Olá, MUI"</span><span class="sxs-lookup"><span data-stu-id="fdf7a-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="fdf7a-336">Embora o exemplo anterior possa exibir sua saída em idiomas diferentes, ele fica curto em várias áreas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="fdf7a-337">Talvez o mais perceptível seja que o aplicativo está disponível apenas em um pequeno subconjunto de linguagens quando comparado ao próprio sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="fdf7a-338">Se, por exemplo, o \_ aplicativo GuiStep 1 da etapa anterior tiver sido instalado em uma compilação japonesa do Windows, as falhas de local de recurso seriam provavelmente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="fdf7a-339">Para resolver essa situação, você tem duas opções principais:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="fdf7a-340">Verifique se os recursos em um idioma de fallback final predeterminado estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="fdf7a-341">Forneça uma maneira para o usuário final configurar suas preferências de idioma entre os subconjuntos de idiomas especificamente suportados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="fdf7a-342">Dessas opções, a que fornece um idioma de fallback final é altamente aconselhável e é implementada neste tutorial passando o sinalizador-g para muirct.exe, como visto acima.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="fdf7a-343">Esse sinalizador informa muirct.exe para fazer uma linguagem específica (de-DE/0x0407) o idioma de fallback final associado ao módulo DLL com neutralidade de idioma (HelloModule.dll).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="fdf7a-344">Em tempo de execução, esse parâmetro é usado como último recurso para gerar texto a ser exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="fdf7a-345">Caso um idioma de fallback final não seja encontrado e nenhum recurso apropriado esteja disponível no binário neutro de idioma, o carregamento do recurso falhará.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="fdf7a-346">Portanto, você deve determinar cuidadosamente os cenários que seu aplicativo pode encontrar e planejar o idioma de fallback final de acordo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="fdf7a-347">A outra opção de permitir preferências de linguagem configuráveis e carregar recursos com base nessa hierarquia definida pelo usuário pode aumentar significativamente a satisfação do cliente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="fdf7a-348">Infelizmente, isso também complica a funcionalidade necessária no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="fdf7a-349">Esta etapa do tutorial usa um mecanismo de arquivo de texto simplificado para habilitar a configuração de idioma do usuário personalizado.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="fdf7a-350">O arquivo de texto é analisado em tempo de execução pelo aplicativo, e a lista de idiomas analisados e validados é usada para estabelecer uma lista de fallback personalizada.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="fdf7a-351">Depois que a lista de fallback personalizada for estabelecida, as APIs do Windows carregarão recursos de acordo com a precedência de idioma definida nesta lista.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="fdf7a-352">O restante do código é semelhante ao encontrado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="fdf7a-353">Adicione um novo projeto à solução HelloMUI (usando o menu seleção arquivo, adicionar e novo projeto) com as seguintes configurações e valores:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="fdf7a-354">Tipo de projeto: projeto Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="fdf7a-355">Nome: GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="fdf7a-356">Local: aceite o padrão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="fdf7a-357">No assistente de aplicativo Win32, selecione o tipo de aplicativo padrão: aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="fdf7a-358">Defina este projeto para ser executado no Visual Studio e configure seu modelo de Threading:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="fdf7a-359">Na Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep \_ 2 e selecione Definir como projeto de inicialização.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="fdf7a-360">Clique com o botão direito do mouse novamente e selecione Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="fdf7a-361">Na caixa de diálogo páginas de propriedades do projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="fdf7a-362">Na lista suspensa superior esquerda, defina configuração para todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="fdf7a-363">Em Propriedades de configuração, expanda C/C++, selecione geração de código e defina biblioteca de tempo de execução: depuração multi-threaded (/MTd).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="fdf7a-364">Substitua o conteúdo de GuiStep \_ 2. cpp pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="fdf7a-365">Crie um arquivo de texto Unicode langs.txt que contenha a seguinte linha:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="fdf7a-366">Certifique-se de salvar o arquivo como Unicode.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="fdf7a-367">Copie langs.txt para o diretório a partir do qual o programa será executado:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="fdf7a-368">Se estiver executando de dentro do Visual Studio, copie-o para *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="fdf7a-369">Se estiver executando do Windows Explorer, copie-o para o mesmo diretório que GuiStep \_2.exe.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="fdf7a-370">Compile e execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-370">Build and run the project.</span></span> <span data-ttu-id="fdf7a-371">Tente editar langs.txt para que os idiomas diferentes apareçam na frente da lista.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="fdf7a-372">Etapa 5: Personalizando "Olá, MUI"</span><span class="sxs-lookup"><span data-stu-id="fdf7a-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="fdf7a-373">Vários dos recursos de tempo de execução mencionados até agora neste tutorial estão disponíveis apenas no Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="fdf7a-374">Talvez você queira reutilizar o esforço investido na localização e na divisão de recursos, fazendo com que o aplicativo funcione em versões de sistema operacional Windows de nível inferior, como o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="fdf7a-375">Esse processo envolve o ajuste do exemplo anterior em duas áreas-chave:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="fdf7a-376">As funções de carregamento de recursos anteriores ao Windows Vista (como [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)e outros) são compatíveis com não-mui.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="fdf7a-377">Os aplicativos que acompanham os recursos divididos (arquivos LN e. mui) devem carregar os módulos de recursos usando uma dessas duas funções:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="fdf7a-378">Se o aplicativo for executado somente no Windows Vista e posterior, ele deverá carregar os módulos de recursos com [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="fdf7a-379">Se o aplicativo for executado em versões anteriores ao Windows Vista, bem como ao Windows Vista ou posterior, ele deverá usar [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), que é uma função de nível inferior específica fornecida no SDK do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="fdf7a-380">O suporte de ordem de fallback de idioma e gerenciamento de idioma oferecido nas versões anteriores do Windows Vista do sistema operacional Windows é diferente do que no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="fdf7a-381">Por esse motivo, os aplicativos que permitem o fallback de idioma configurado pelo usuário devem ajustar suas práticas de gerenciamento de idioma:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="fdf7a-382">Se o aplicativo for executado somente no Windows Vista e posterior, a configuração da lista de idiomas usando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) será suficiente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="fdf7a-383">Se o aplicativo for executado em todas as versões do Windows, será necessário construir o código que será executado em plataformas de nível inferior para iterar pela lista de idiomas configurados pelo usuário e investigação do módulo de recurso desejado.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="fdf7a-384">Isso pode ser visto nas seções 1C e 2 do código fornecido posteriormente nesta etapa.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="fdf7a-385">Crie um projeto que possa usar os módulos de recursos localizados em qualquer versão do Windows:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="fdf7a-386">Adicione um novo projeto à solução HelloMUI (usando o menu seleção arquivo, adicionar e novo projeto) com as seguintes configurações e valores:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="fdf7a-387">Tipo de projeto: projeto Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="fdf7a-388">Nome: GuiStep \_ 3.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="fdf7a-389">Local: aceite o padrão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="fdf7a-390">No assistente de aplicativo Win32, selecione o tipo de aplicativo padrão: aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="fdf7a-391">Defina este projeto para ser executado no Visual Studio e configure seu modelo de Threading.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="fdf7a-392">Além disso, configure-o para adicionar os cabeçalhos e as bibliotecas necessários.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="fdf7a-393">Os caminhos usados neste tutorial pressupõem que o SDK do Windows 7 e o pacote de APIs de nível inferior do Microsoft NLS foram instalados em seus diretórios padrão.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="fdf7a-394">Se esse não for o caso, modifique os caminhos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="fdf7a-395">Na Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep \_ 3 e selecione Definir como projeto de inicialização.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="fdf7a-396">Clique com o botão direito do mouse novamente e selecione Propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="fdf7a-397">Na caixa de diálogo páginas de propriedades do projeto:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="fdf7a-398">Na lista suspensa superior esquerda, defina configuração para todas as configurações.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="fdf7a-399">Em Propriedades de configuração, expanda C/C++, selecione geração de código e defina biblioteca de tempo de execução: depuração multi-threaded (/MTd).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="fdf7a-400">Selecione geral e adicione aos diretórios de inclusão adicionais:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="fdf7a-401">"C: as \\ APIs de nível inferior do Microsoft NLS \\ incluem".</span><span class="sxs-lookup"><span data-stu-id="fdf7a-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="fdf7a-402">Selecione idioma e defina tratar WCHAR \_ t como tipo interno: não (/Zc: WCHAR \_ t-).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="fdf7a-403">Selecione avançado e defina a Convenção de chamada: \_ stdcall (/gz).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="fdf7a-404">Em Propriedades de configuração, expanda vinculador, selecione entrada e adicionar a dependências adicionais:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="fdf7a-405">"C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ lib \\ MUILoad. lib".</span><span class="sxs-lookup"><span data-stu-id="fdf7a-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="fdf7a-406">"C: \\ APIs de nível inferior da Microsoft NLS \\ \\ x86 \\ nlsdl. lib".</span><span class="sxs-lookup"><span data-stu-id="fdf7a-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="fdf7a-407">Substitua o conteúdo de GuiStep \_ 3. cpp pelo código a seguir:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="fdf7a-408">Crie ou copie langs.txt para o diretório apropriado, conforme descrito anteriormente na [etapa 4: Globalizando "Hello mui"](#step-4-globalizing-hello-mui).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="fdf7a-409">Compile e execute o projeto.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="fdf7a-410">Se o aplicativo deve ser executado em versões do Windows anteriores ao Windows Vista, leia os documentos que vieram com o pacote de [APIs de nível inferior do Microsoft NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) sobre como redistribuir Nlsdl.dll.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="fdf7a-411">Considerações adicionais sobre o MUI</span><span class="sxs-lookup"><span data-stu-id="fdf7a-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="fdf7a-412">Suporte para aplicativos de console</span><span class="sxs-lookup"><span data-stu-id="fdf7a-412">Support for Console Applications</span></span>

<span data-ttu-id="fdf7a-413">As técnicas abordadas neste tutorial também podem ser usadas em aplicativos de console.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="fdf7a-414">No entanto, ao contrário da maioria dos controles de GUI padrão, a janela de comando do Windows não pode exibir caracteres para todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="fdf7a-415">Por esse motivo, os aplicativos de console multilíngües exigem atenção especial.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="fdf7a-416">Chamar as APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) ou [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) com sinalizadores de filtragem específicos faz com que as funções de carregamento de recursos removam as investigações de recursos de idioma para linguagens específicas que normalmente não são exibidas em uma janela de comando.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="fdf7a-417">Quando esses sinalizadores são definidos, os algoritmos de configuração de idioma permitem apenas os idiomas que serão exibidos corretamente na janela de comando para que fiquem na lista de fallback.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="fdf7a-418">Para obter mais informações sobre como usar essas APIs para criar um aplicativo de console multilíngüe, consulte as seções comentários de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) e [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="fdf7a-419">Determinação de idiomas para suporte em Run-Time</span><span class="sxs-lookup"><span data-stu-id="fdf7a-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="fdf7a-420">Você pode adotar uma das seguintes sugestões de design para determinar em quais idiomas seu aplicativo deve dar suporte em tempo de execução:</span><span class="sxs-lookup"><span data-stu-id="fdf7a-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="fdf7a-421">**Durante a instalação, habilite o usuário final para selecionar o idioma preferencial em uma lista de idiomas com suporte**</span><span class="sxs-lookup"><span data-stu-id="fdf7a-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="fdf7a-422">**Ler uma lista de idiomas de um arquivo de configuração**</span><span class="sxs-lookup"><span data-stu-id="fdf7a-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="fdf7a-423">Alguns dos projetos neste tutorial contêm uma função usada para analisar um arquivo de configuração langs.txt, que contém uma lista de idiomas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="fdf7a-424">Como essa função usa entrada externa, valide os idiomas que são fornecidos como entrada.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="fdf7a-425">Consulte as funções [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) ou [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) para obter mais detalhes sobre como executar essa validação.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="fdf7a-426">**Consultar o sistema operacional para determinar quais idiomas estão instalados**</span><span class="sxs-lookup"><span data-stu-id="fdf7a-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="fdf7a-427">Essa abordagem ajuda o aplicativo a usar o mesmo idioma que o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="fdf7a-428">Embora isso não exija a solicitação do usuário, se você escolher essa opção, lembre-se de que os idiomas do sistema operacional podem ser adicionados ou removidos a qualquer momento e podem ser alterados após o usuário instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="fdf7a-429">Além disso, lembre-se de que, em alguns casos, o sistema operacional é instalado com suporte a idiomas limitados e o aplicativo oferece mais valor se oferecer suporte a idiomas para os quais o sistema operacional não oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="fdf7a-430">Para obter mais informações sobre como determinar os idiomas atualmente instalados no sistema operacional, consulte a função [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .</span><span class="sxs-lookup"><span data-stu-id="fdf7a-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="fdf7a-431">Suporte a scripts complexos em versões anteriores ao Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdf7a-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="fdf7a-432">Quando um aplicativo que dá suporte a determinados scripts complexos é executado em uma versão do Windows anterior ao Windows Vista, o texto nesse script pode não ser exibido corretamente em componentes de GUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="fdf7a-433">Por exemplo, no projeto de nível inferior neste tutorial, os scripts de hi-IN e ta-IN podem não ser exibidos na caixa de mensagem devido a problemas com o processamento de scripts complexos e a falta de fontes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="fdf7a-434">Normalmente, os problemas dessa natureza se apresentam como caixas quadradas no componente da GUI.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="fdf7a-435">Mais informações sobre como habilitar o processamento de script complexo podem ser encontradas em [suporte a scripts e fontes no Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="fdf7a-436">Resumo</span><span class="sxs-lookup"><span data-stu-id="fdf7a-436">Summary</span></span>

<span data-ttu-id="fdf7a-437">Este tutorial globalizava um aplicativo multilíngue e demonstrou as práticas recomendadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="fdf7a-438">Projete o aplicativo para aproveitar o modelo de recurso do Win32.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="fdf7a-439">Utilize a divisão de recursos do MUI em binários satélite (arquivos. mui).</span><span class="sxs-lookup"><span data-stu-id="fdf7a-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="fdf7a-440">Verifique se o processo de localização atualiza os recursos nos arquivos. mui para que sejam apropriados para o idioma de destino.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="fdf7a-441">Certifique-se de que o empacotamento e a implantação do aplicativo, arquivos. mui associados e conteúdo de configuração seja feito corretamente para permitir que as APIs de carregamento de recursos localizem o conteúdo localizado.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="fdf7a-442">Forneça ao usuário final um mecanismo para ajustar a configuração de idioma do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="fdf7a-443">Ajuste o código de tempo de execução para aproveitar a configuração da linguagem, para tornar o aplicativo mais responsivo às necessidades dos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="fdf7a-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
