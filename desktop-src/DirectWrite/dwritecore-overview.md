---
title: Visão geral do DWriteCore
description: DWriteCore é a implementação Windows SDK do Aplicativo DirectWrite.
keywords:
- DirectWrite Núcleo
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 644ce3c5715e1cc57129b36047169c20e80a6697
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689189"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="db170-105">Visão geral do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-105">DWriteCore overview</span></span>

<span data-ttu-id="db170-106">DWriteCore é a implementação do [SDK](/windows/apps/windows-app-sdk/) do aplicativo Windows do DirectWrite (DirectWrite é [a](./direct-write-portal.md) API do DirectX para renderização de texto de alta qualidade, fontes de estrutura de contorno independentes de resolução e suporte completo a texto e layout Unicode).</span><span class="sxs-lookup"><span data-stu-id="db170-106">DWriteCore is the [Windows App SDK](/windows/apps/windows-app-sdk/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="db170-107">DWriteCore é uma forma de DirectWrite que é executado em versões do Windows até Windows 10, versão 1809 (10.0; Build 17763) e abre a porta para você usá-lo em plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="db170-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="db170-108">Este tópico introdutório descreve o que é o DWriteCore e mostra como instalá-lo em seu ambiente dev e programa com ele.</span><span class="sxs-lookup"><span data-stu-id="db170-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

> [!TIP]
> <span data-ttu-id="db170-109">Para ver descrições de e links para componentes do DirectX no desenvolvimento ativo, consulte a postagem no blog Página de aterrissagem [do DirectX](https://devblogs.microsoft.com/directx/landing-page/).</span><span class="sxs-lookup"><span data-stu-id="db170-109">For descriptions of and links to DirectX components in active development, see the blog post [DirectX Landing Page](https://devblogs.microsoft.com/directx/landing-page/).</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="db170-110">A proposta de valor de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-110">The value proposition of DWriteCore</span></span>

<span data-ttu-id="db170-111">[DirectWrite](./direct-write-portal.md) em si dá suporte a uma ampla variedade de recursos que a torna a ferramenta de renderização de fonte de sua escolha no Windows para a maioria dos aplicativos, seja por meio de chamadas diretas ou por meio &mdash; [de Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="db170-111">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="db170-112">DirectWrite inclui um sistema de layout de texto independente de dispositivo, renderização de texto [Microsoft ClearType](/typography/cleartype/) de sub pixel de alta qualidade, texto acelerado por hardware, texto de vários formatos, recursos avançados de [tipografia OpenType®](/typography/opentype/) suporte a linguagem ampla e layout e renderização compatíveis com [GDI.](../gdi/windows-gdi.md)</span><span class="sxs-lookup"><span data-stu-id="db170-112">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="db170-113">DirectWrite está disponível desde o Windows Vista SP2 e evoluiu ao longo dos anos para incluir recursos mais avançados, como fontes variáveis, o que permite aplicar estilos, pesos e outros atributos a uma fonte com apenas um recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="db170-113">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="db170-114">No entanto, devido ao longo período de vida DirectWrite, os avanços no desenvolvimento tendem a deixar versões mais antigas do Windows para trás.</span><span class="sxs-lookup"><span data-stu-id="db170-114">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="db170-115">Além disso, o status DirectWrite como a tecnologia de renderização de texto premier é limitado apenas ao Windows, deixando os aplicativos de plataforma cruzada escreverem sua própria pilha de renderização de texto ou dependerem de soluções de terceiros.</span><span class="sxs-lookup"><span data-stu-id="db170-115">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="db170-116">DWriteCore resolve os problemas fundamentais de compatibilidade de recursos de versão órfãos e multiplatafa removendo a biblioteca do sistema e direcionando todos os pontos de extremidade com suporte possíveis.</span><span class="sxs-lookup"><span data-stu-id="db170-116">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="db170-117">Para esse fim, integramos o DWriteCore ao SDK Windows Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db170-117">To that end, we've integrated DWriteCore into Windows App SDK.</span></span>

<span data-ttu-id="db170-118">O principal valor que o DWriteCore fornece, como desenvolvedor, no SDK do aplicativo Windows é que ele fornece acesso a muitos recursos (e, eventualmente, todos) DirectWrite recursos.</span><span class="sxs-lookup"><span data-stu-id="db170-118">The primary value that DWriteCore gives you, as a developer, in Windows App SDK is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="db170-119">Todos os recursos do DWriteCore funcionarão da mesma forma em todas as versões de nível inferior sem qualquer disparidade sobre quais recursos podem funcionar em quais versões.</span><span class="sxs-lookup"><span data-stu-id="db170-119">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="db170-120">O aplicativo de demonstração &mdash; DWriteCore DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="db170-120">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="db170-121">DWriteCore é demonstrado por meio do aplicativo de exemplo [DWriteCoreGallery,](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) que está disponível para download e estudo.</span><span class="sxs-lookup"><span data-stu-id="db170-121">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="db170-122">Começar a trabalhar com DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-122">Get started with DWriteCore</span></span>

<span data-ttu-id="db170-123">O DWriteCore faz parte [Windows SDK do Aplicativo 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span><span class="sxs-lookup"><span data-stu-id="db170-123">DWriteCore is part of [Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span></span> <span data-ttu-id="db170-124">Esta seção descreve como configurar seu ambiente de desenvolvimento para programação com DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="db170-124">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-windows-app-sdk-08-vsix"></a><span data-ttu-id="db170-125">Instalar o Windows SDK do Aplicativo 0.8 VSIX</span><span class="sxs-lookup"><span data-stu-id="db170-125">Install the Windows App SDK 0.8 VSIX</span></span>

<span data-ttu-id="db170-126">No Visual Studio, clique em **Extensões** Gerenciar Extensões, pesquise Windows SDK do Aplicativo e baixe a  >  extensão Windows SDK do Aplicativo. </span><span class="sxs-lookup"><span data-stu-id="db170-126">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Windows App SDK*, and download the Windows App SDK extension.</span></span> <span data-ttu-id="db170-127">Feche e reabra Visual Studio e siga os prompts para instalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="db170-127">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="db170-128">Para obter mais informações, [consulte Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) [e Configurar seu ambiente de desenvolvimento](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="db170-128">For more info, see [Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0) and [Set up your development environment](/windows/apps/windows-app-sdk/set-up-your-development-environment#3-install-the-windows-app-sdk-extension-for-visual-studio).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="db170-129">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="db170-129">Create a new project</span></span>

<span data-ttu-id="db170-130">No Visual Studio, crie um novo projeto do modelo de projeto Aplicativo em **Branco, Empacotado (WinUI 3 na Área de Trabalho).**</span><span class="sxs-lookup"><span data-stu-id="db170-130">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="db170-131">Você pode encontrar esse modelo de projeto escolhendo o idioma: *C++;* platform: *Windows SDK do Aplicativo;* tipo de projeto: *Área de Trabalho.*</span><span class="sxs-lookup"><span data-stu-id="db170-131">You can find that project template by choosing language: *C++*; platform: *Windows App SDK*; project type: *Desktop*.</span></span>

<span data-ttu-id="db170-132">Para obter mais informações, [consulte Project modelos para WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span><span class="sxs-lookup"><span data-stu-id="db170-132">For more info, see [Project templates for WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="db170-133">Instalar o pacote de NuGet Microsoft.ProjectReunion.DWrite</span><span class="sxs-lookup"><span data-stu-id="db170-133">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="db170-134">No Visual Studio, clique em **Project** Gerenciar pacotes do NuGet... Procure , digite ou colar \>  \>  **Microsoft.ProjectReunion.DWrite**  na caixa de pesquisa, selecione o item nos resultados da pesquisa e clique em Instalar para instalar o pacote para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="db170-134">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="db170-135">Como alternativa, comece com o aplicativo de exemplo DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="db170-135">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="db170-136">Como alternativa, você pode programar com DWriteCore começando com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) e basear seu desenvolvimento nesse projeto.</span><span class="sxs-lookup"><span data-stu-id="db170-136">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/WindowsAppSDK-Samples/tree/main/Samples/TextRendering) sample app project, and base your development on that project.</span></span> <span data-ttu-id="db170-137">Em seguida, você pode se sentir à vontade para remover qualquer código-fonte (ou arquivos) existente desse projeto de exemplo e adicionar qualquer novo código-fonte (ou arquivos) ao projeto.</span><span class="sxs-lookup"><span data-stu-id="db170-137">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="db170-138">Usar DWriteCore em seu projeto</span><span class="sxs-lookup"><span data-stu-id="db170-138">Use DWriteCore in your project</span></span>

<span data-ttu-id="db170-139">Para obter mais informações sobre programação com DWriteCore, consulte a [seção Programação com DWriteCore](#programming-with-dwritecore) mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="db170-139">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="db170-140">As fases de lançamento do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-140">The release phases of DWriteCore</span></span>

<span data-ttu-id="db170-141">A porta DirectWrite para DWriteCore é um projeto suficientemente grande para abranger vários Windows de lançamento.</span><span class="sxs-lookup"><span data-stu-id="db170-141">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="db170-142">Esse projeto é dividido em fases, cada uma correspondendo a uma parte da funcionalidade entregue em uma versão.</span><span class="sxs-lookup"><span data-stu-id="db170-142">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="db170-143">Recursos na versão atual do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-143">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="db170-144">A versão do DWriteCore disponível atualmente faz parte [Windows SDK do Aplicativo 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span><span class="sxs-lookup"><span data-stu-id="db170-144">The version of DWriteCore currently available is part of [Windows App SDK 0.8](https://github.com/microsoft/ProjectReunion/releases/tag/v0.8.0).</span></span> <span data-ttu-id="db170-145">Ele contém as ferramentas básicas que você, como desenvolvedor, precisa consumir DWriteCore, incluindo os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="db170-145">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="db170-146">Enumeração de fonte.</span><span class="sxs-lookup"><span data-stu-id="db170-146">Font enumeration.</span></span>
- <span data-ttu-id="db170-147">API de fonte.</span><span class="sxs-lookup"><span data-stu-id="db170-147">Font API.</span></span>
- <span data-ttu-id="db170-148">Moldar.</span><span class="sxs-lookup"><span data-stu-id="db170-148">Shaping.</span></span>
- <span data-ttu-id="db170-149">APIs de renderização de baixo nível.</span><span class="sxs-lookup"><span data-stu-id="db170-149">Low-level rendering APIs.</span></span> <span data-ttu-id="db170-150">Isso é parcial na fase atual O DWriteCore não interopera com o Direct2D , mas você pode usar &mdash; [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget). [](../direct2d/direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="db170-150">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="db170-151">Funcionalidade básica de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="db170-151">Basic text layout functionality.</span></span>
- <span data-ttu-id="db170-152">APIs de renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="db170-152">Text-rendering APIs.</span></span>
- <span data-ttu-id="db170-153">Destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="db170-153">Bitmap render target.</span></span>
- <span data-ttu-id="db170-154">Fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="db170-154">Color fonts.</span></span>
- <span data-ttu-id="db170-155">Otimizações diversas (limpeza de cache de fonte, carregador de fonte na memória e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="db170-155">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>
- <span data-ttu-id="db170-156">Suporte para &mdash; sublinhado consulte [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) e [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline).</span><span class="sxs-lookup"><span data-stu-id="db170-156">Support for underline&mdash;see [**IDWriteTextLayout::GetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getunderline) and [**IDWriteTextLayout::SetUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setunderline).</span></span>
- <span data-ttu-id="db170-157">Suporte para tachado &mdash; consulte [**IDWriteTextLayout::GetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) e [**IDWriteTextLayout::SetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough).</span><span class="sxs-lookup"><span data-stu-id="db170-157">Support for strikethrough&mdash;see [**IDWriteTextLayout::GetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough) and [**IDWriteTextLayout::SetStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough).</span></span>
- <span data-ttu-id="db170-158">Suporte para texto vertical por [**meio de IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) &mdash; consulte Texto [vertical](/windows/win32/directwrite/vertical-text).</span><span class="sxs-lookup"><span data-stu-id="db170-158">Support for vertical text via [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)&mdash;see [Vertical text](/windows/win32/directwrite/vertical-text).</span></span>
- <span data-ttu-id="db170-159">Todos os métodos das interfaces [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) e [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) são implementados.</span><span class="sxs-lookup"><span data-stu-id="db170-159">All of the methods of the [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) and [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) interfaces are implemented.</span></span>

<span data-ttu-id="db170-160">Um recurso de faixa são fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="db170-160">A banner feature is color fonts.</span></span> <span data-ttu-id="db170-161">As fontes de cores permitem renderizar suas fontes com funcionalidades de cores mais sofisticadas além de cores simples.</span><span class="sxs-lookup"><span data-stu-id="db170-161">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="db170-162">Por exemplo, fontes de cores é o que alimenta a capacidade de renderizar fontes de ícone de barra de ferramentas e emoji (a última das quais é usada por Office, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="db170-162">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="db170-163">As fontes de cores foram introduzidas pela primeira vez no Windows 8.1, mas o recurso foi muito expandido no Windows 10, versão 1607 (Atualização de Aniversário).</span><span class="sxs-lookup"><span data-stu-id="db170-163">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="db170-164">O trabalho na limpeza do cache de fontes e no carregador de fontes na memória permitem o carregamento mais rápido de fontes e aprimoramentos de memória.</span><span class="sxs-lookup"><span data-stu-id="db170-164">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="db170-165">Com esses recursos, você pode começar imediatamente a aproveitar algumas das funcionalidades básicas modernas do DirectWrite, como &mdash; fontes variáveis.</span><span class="sxs-lookup"><span data-stu-id="db170-165">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="db170-166">As fontes de variável são um dos recursos mais importantes para DirectWrite clientes.</span><span class="sxs-lookup"><span data-stu-id="db170-166">Variable fonts are one of the most important features for DirectWrite customers.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="db170-167">Nosso convite para você como desenvolvedor DirectWrite aplicativo</span><span class="sxs-lookup"><span data-stu-id="db170-167">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="db170-168">O DWriteCore, juntamente com outros Windows componentes do SDK do Aplicativo, serão desenvolvidos com abertura aos comentários dos desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="db170-168">DWriteCore, along with other Windows App SDK components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="db170-169">Convidamos você a começar a explorar o DWriteCore e fornecer insights ou solicitações sobre o desenvolvimento de recursos em nosso repositório GitHub [SDK](https://github.com/microsoft/ProjectReunion/)de Aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="db170-169">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Windows App SDK GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="db170-170">Programação com DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-170">Programming with DWriteCore</span></span>

<span data-ttu-id="db170-171">Assim como com [DirectWrite](./direct-write-portal.md), você programa com DWriteCore por meio de sua API com luz COM, por meio da interface [**IDWriteFactory.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)</span><span class="sxs-lookup"><span data-stu-id="db170-171">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="db170-172">Para usar DWriteCore, é necessário incluir o `dwrite_core.h` arquivo de header.</span><span class="sxs-lookup"><span data-stu-id="db170-172">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="db170-173">O `dwrite_core.h` arquivo de título primeiro define o token *DWRITE_CORE* e, em seguida, inclui o arquivo `dwrite_3.h` de título.</span><span class="sxs-lookup"><span data-stu-id="db170-173">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="db170-174">O *DWRITE_CORE* token é importante, pois ele direciona todos os headers subsequentemente incluídos para disponibilizar todas as APIs DirectWrite para você.</span><span class="sxs-lookup"><span data-stu-id="db170-174">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="db170-175">Depois que o projeto tiver incluído , você poderá continuar `dwrite_core.h` e escrever código, criar e executar.</span><span class="sxs-lookup"><span data-stu-id="db170-175">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="db170-176">APIs novas ou diferentes para DWriteCore</span><span class="sxs-lookup"><span data-stu-id="db170-176">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="db170-177">A superfície da API DWriteCore é a mesma para DirectWrite [.](/windows/win32/api/_directwrite/)</span><span class="sxs-lookup"><span data-stu-id="db170-177">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="db170-178">Mas há um pequeno número de novas APIs que estão apenas em DWriteCore no momento.</span><span class="sxs-lookup"><span data-stu-id="db170-178">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="db170-179">Criar um objeto de fábrica</span><span class="sxs-lookup"><span data-stu-id="db170-179">Create a factory object</span></span>

<span data-ttu-id="db170-180">A [**função livre DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.</span><span class="sxs-lookup"><span data-stu-id="db170-180">The [**DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="db170-181">**DWriteCoreCreateFactory** é funcionalmente o mesmo que a [função DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="db170-181">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="db170-182">A função DWriteCore tem um nome diferente para evitar ambiguidade.</span><span class="sxs-lookup"><span data-stu-id="db170-182">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="db170-183">Criar um objeto de fábrica restrito</span><span class="sxs-lookup"><span data-stu-id="db170-183">Create a restricted factory object</span></span>

<span data-ttu-id="db170-184">A [**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type) enumeração tem uma nova constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indicando uma fábrica restrita.</span><span class="sxs-lookup"><span data-stu-id="db170-184">The [**DWRITE_FACTORY_TYPE**](/windows/windows-app-sdk/api/win32/dwrite/ne-dwrite-dwrite_factory_type) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="db170-185">Uma fábrica restrita é mais bloqueada do que uma fábrica isolada.</span><span class="sxs-lookup"><span data-stu-id="db170-185">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="db170-186">Ele não interage com um cache de fontes persistente nem entre processos de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="db170-186">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="db170-187">Além disso, a coleção de fontes do sistema retornada dessa fábrica inclui apenas fontes conhecidas.</span><span class="sxs-lookup"><span data-stu-id="db170-187">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="db170-188">Veja como você pode usar o **DWRITE_FACTORY_TYPE_ISOLATED2** criar um objeto de fábrica restrito ao chamar a função livre [**DWriteCoreCreateFactory.**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory)</span><span class="sxs-lookup"><span data-stu-id="db170-188">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](/windows/windows-app-sdk/api/win32/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="db170-189">Se você passar **DWRITE_FACTORY_TYPE_ISOLATED2** para uma versão mais antiga do DirectWrite que não dá suporte a ela, **DWriteCreateFactory** retornará **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="db170-189">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="db170-190">Desenhando glifos em um bitmap de memória do sistema</span><span class="sxs-lookup"><span data-stu-id="db170-190">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="db170-191">DirectWrite tem uma interface de destino de renderização de bitmap que dá suporte à renderização de glifos em um bitmap na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="db170-191">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="db170-192">No entanto, atualmente, a única maneira de obter acesso aos dados de pixel subjacente é passar pela GDI e, portanto, a API não pode ser usada entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="db170-192">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="db170-193">Isso é facilmente corrigido adicionando um método para recuperar os dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="db170-193">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="db170-194">Portanto, dWriteCore introduz a interface [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) e seu método [**IDWriteBitmapRenderTarget2::GetBitmapData**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata).</span><span class="sxs-lookup"><span data-stu-id="db170-194">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](/windows/windows-app-sdk/api/win32/dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata).</span></span> <span data-ttu-id="db170-195">Esse método recebe um parâmetro do tipo (ponteiro para) [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), que é um novo struct.</span><span class="sxs-lookup"><span data-stu-id="db170-195">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32), which is a new struct.</span></span>

<span data-ttu-id="db170-196">Seu aplicativo cria um destino de renderização de bitmap chamando [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="db170-196">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="db170-197">No Windows, um destino de renderização de bitmap encapsula um DC de memória GDI com um DIB (bitmap independente de dispositivo) GDI selecionado nele.</span><span class="sxs-lookup"><span data-stu-id="db170-197">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="db170-198">[IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renderiza glifos para o DIB.</span><span class="sxs-lookup"><span data-stu-id="db170-198">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="db170-199">DirectWrite renderiza os glifos em si sem passar pela GDI.</span><span class="sxs-lookup"><span data-stu-id="db170-199">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="db170-200">Em seguida, seu aplicativo pode obter o **HDC** do destino de renderização de bitmap e usar [o BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar os pixels para um **HDC de janela.**</span><span class="sxs-lookup"><span data-stu-id="db170-200">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="db170-201">Em plataformas não Windows, seu aplicativo ainda pode criar um destino de renderização de bitmap, mas ele simplesmente encapsula uma matriz de memória do sistema sem **HDC** e sem DIB.</span><span class="sxs-lookup"><span data-stu-id="db170-201">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="db170-202">Sem um **HDC**, deve haver outra maneira para seu aplicativo obter os pixels de bitmap para que ele possa copiá-los ou usá-los de outra forma.</span><span class="sxs-lookup"><span data-stu-id="db170-202">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="db170-203">Mesmo Windows, às vezes é útil obter os dados de pixel reais e mostramos a maneira atual de fazer isso no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="db170-203">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="db170-204">Outras diferenças de API entre DWriteCore e DirectWrite</span><span class="sxs-lookup"><span data-stu-id="db170-204">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="db170-205">Há algumas APIs que são apenas stubs ou que se comportam de forma um pouco diferente em plataformas Windows diferentes.</span><span class="sxs-lookup"><span data-stu-id="db170-205">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="db170-206">Por exemplo, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retorna E_NOTIMPL em plataformas não Windows, já que não há nenhum **HDC** sem [GDI.](../gdi/windows-gdi.md) </span><span class="sxs-lookup"><span data-stu-id="db170-206">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="db170-207">E, por fim, há algumas outras APIs Windows que normalmente são usadas junto com DirectWrite (Direct2D sendo um exemplo notável).</span><span class="sxs-lookup"><span data-stu-id="db170-207">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="db170-208">No entanto, atualmente, Direct2D e DWriteCore não interoperam.</span><span class="sxs-lookup"><span data-stu-id="db170-208">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="db170-209">Por exemplo, se você criar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e passá-lo para [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="db170-209">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
