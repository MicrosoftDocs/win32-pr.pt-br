---
title: Visão geral do DWriteCore
description: DWriteCore é a implementação de reunião do projeto de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 0f908f000d340f9cc9f374e036919422c4a940a6
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262638"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="d9a53-105">Visão geral do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-105">DWriteCore overview</span></span>

<span data-ttu-id="d9a53-106">DWriteCore é a implementação de [reunião do projeto](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md) (DirectWrite é a API do DirectX para renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto Unicode e layout).</span><span class="sxs-lookup"><span data-stu-id="d9a53-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="d9a53-107">DWriteCore é uma forma de DirectWrite que é executada em versões do Windows até o Windows 10, versão 1809 (10,0; Build 17763) e abre a porta para você usá-la entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="d9a53-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 10, version 1809 (10.0; Build 17763), and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="d9a53-108">Este tópico introdutório descreve o que é o DWriteCore e mostra como instalá-lo em seu ambiente de desenvolvimento e programar com ele.</span><span class="sxs-lookup"><span data-stu-id="d9a53-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

> [!TIP]
> <span data-ttu-id="d9a53-109">Para obter descrições e links para componentes do DirectX em desenvolvimento ativo, consulte a postagem do blog [página inicial do DirectX](https://devblogs.microsoft.com/directx/landing-page/).</span><span class="sxs-lookup"><span data-stu-id="d9a53-109">For descriptions of and links to DirectX components in active development, see the blog post [DirectX Landing Page](https://devblogs.microsoft.com/directx/landing-page/).</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="d9a53-110">A proposta de valor de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-110">The value proposition of DWriteCore</span></span>

<span data-ttu-id="d9a53-111">O [DirectWrite](./direct-write-portal.md) em si dá suporte a uma ampla gama de recursos que o torna a ferramenta de renderização de fontes de escolha no Windows para a maioria dos aplicativos &mdash; , seja por meio de chamadas diretas ou por meio de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="d9a53-111">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="d9a53-112">O DirectWrite inclui um sistema de layout de texto independente de dispositivo, renderização de texto de alta qualidade de subpixel [do Microsoft ClearType](/typography/cleartype/) , texto acelerado por hardware, texto de vários formatos, recursos de tipografia de [® de OpenType](/typography/opentype/) avançados, suporte a todo o idioma e renderização e processamento compatíveis com [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="d9a53-112">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="d9a53-113">O DirectWrite está disponível desde o Windows Vista SP2 e evoluiu ao longo dos anos para incluir recursos mais avançados, como fontes variáveis, que permitem aplicar estilos, pesos e outros atributos a uma fonte com apenas um recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="d9a53-113">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables you to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="d9a53-114">No entanto, devido à longa vida útil do DirectWrite, os avanços no desenvolvimento têm o tendiam de deixar versões anteriores do Windows atrás.</span><span class="sxs-lookup"><span data-stu-id="d9a53-114">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="d9a53-115">Além disso, o status do DirectWrite como a tecnologia de renderização de texto Premier é limitado apenas ao Windows, deixando aplicativos de plataforma cruzada para gravar sua própria pilha de renderização de texto ou para se basear em soluções de terceiros.</span><span class="sxs-lookup"><span data-stu-id="d9a53-115">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="d9a53-116">O DWriteCore resolve os problemas fundamentais de órfão de recursos de versão e compatibilidade entre plataformas removendo a biblioteca do sistema e direcionando todos os pontos de extremidade possíveis com suporte.</span><span class="sxs-lookup"><span data-stu-id="d9a53-116">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="d9a53-117">Para esse fim, integramos o DWriteCore à reunião do projeto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-117">To that end, we've integrated DWriteCore into Project Reunion.</span></span>

<span data-ttu-id="d9a53-118">O valor principal que o DWriteCore fornece a você, como desenvolvedor, na reunião do projeto, é que ele fornece acesso a muitos (e eventualmente todos) recursos do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9a53-118">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to many (and eventually all) DirectWrite features.</span></span> <span data-ttu-id="d9a53-119">Todos os recursos do DWriteCore funcionarão da mesma forma em todas as versões de nível inferior, sem qualquer diferença em relação a quais recursos podem funcionar em quais versões.</span><span class="sxs-lookup"><span data-stu-id="d9a53-119">All features of DWriteCore will function the same on all down-level versions without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="d9a53-120">O aplicativo de demonstração DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="d9a53-120">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="d9a53-121">O DWriteCore é demonstrado por meio do aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que está disponível para você agora para baixar e estudar.</span><span class="sxs-lookup"><span data-stu-id="d9a53-121">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="d9a53-122">Introdução ao DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-122">Get started with DWriteCore</span></span>

<span data-ttu-id="d9a53-123">DWriteCore faz parte do [projeto reunião 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="d9a53-123">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="d9a53-124">Esta seção descreve como configurar seu ambiente de desenvolvimento para a programação com o DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="d9a53-124">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="d9a53-125">Instalar o VSIX do projeto reunião 0,5</span><span class="sxs-lookup"><span data-stu-id="d9a53-125">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="d9a53-126">No Visual Studio, clique em **extensões**  >  **gerenciar extensões**, pesquise por *reunião do projeto* e baixe a extensão de reunião do projeto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-126">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="d9a53-127">Feche e reabra o Visual Studio e siga os prompts para instalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="d9a53-127">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="d9a53-128">Para obter mais informações, consulte [reunião do projeto 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)e [configurar seu ambiente de desenvolvimento (para a reunião do projeto)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span><span class="sxs-lookup"><span data-stu-id="d9a53-128">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Set up your development environment (for Project Reunion)](/windows/apps/project-reunion/get-started-with-project-reunion#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="d9a53-129">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="d9a53-129">Create a new project</span></span>

<span data-ttu-id="d9a53-130">No Visual Studio, crie um novo projeto do modelo de projeto **aplicativo em branco, empacotado (WinUI 3 no desktop)** .</span><span class="sxs-lookup"><span data-stu-id="d9a53-130">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="d9a53-131">Você pode encontrar esse modelo de projeto escolhendo linguagem: *C++*; plataforma: *reunião do projeto*; tipo de projeto: *área de trabalho*.</span><span class="sxs-lookup"><span data-stu-id="d9a53-131">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="d9a53-132">Para obter mais informações, consulte Introdução [ao WinUI 3 para aplicativos da área de trabalho](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span><span class="sxs-lookup"><span data-stu-id="d9a53-132">For more info, see [Get started with WinUI 3 for desktop apps](/windows/apps/winui/winui3/get-started-winui3-for-desktop).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="d9a53-133">Instalar o pacote NuGet Microsoft. ProjectReunion. DWrite</span><span class="sxs-lookup"><span data-stu-id="d9a53-133">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="d9a53-134">No Visual Studio, clique em **projeto** \> **gerenciar pacotes NuGet...** \> **procure**, digite ou cole **Microsoft. ProjectReunion. DWrite** na caixa de pesquisa, selecione o item nos resultados da pesquisa e clique em **instalar** para instalar o pacote para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-134">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="d9a53-135">Como alternativa, comece com o aplicativo de exemplo DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="d9a53-135">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="d9a53-136">Como alternativa, você pode programar com DWriteCore começando com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basear seu desenvolvimento nesse projeto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-136">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="d9a53-137">Você pode, então, ficar à vontade para remover qualquer código-fonte (ou arquivos) existente desse projeto de exemplo e adicionar qualquer código-fonte (ou arquivos) novo ao projeto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-137">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="d9a53-138">Usar o DWriteCore em seu projeto</span><span class="sxs-lookup"><span data-stu-id="d9a53-138">Use DWriteCore in your project</span></span>

<span data-ttu-id="d9a53-139">Para obter mais informações sobre programação com o DWriteCore, consulte a seção [programação com DWriteCore](#programming-with-dwritecore) mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="d9a53-139">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="d9a53-140">As fases de lançamento do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-140">The release phases of DWriteCore</span></span>

<span data-ttu-id="d9a53-141">Portar DirectWrite para DWriteCore é um projeto suficientemente grande para abranger vários ciclos de versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="d9a53-141">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="d9a53-142">Esse projeto é dividido em fases, cada uma correspondendo a uma parte da funcionalidade fornecida em uma versão.</span><span class="sxs-lookup"><span data-stu-id="d9a53-142">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="d9a53-143">Recursos na versão atual do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-143">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="d9a53-144">A versão do DWriteCore atualmente disponível faz parte do [projeto reunião 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="d9a53-144">The version of DWriteCore currently available is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="d9a53-145">Ele contém as ferramentas básicas que você, como desenvolvedor, precisam consumir o DWriteCore, incluindo os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9a53-145">It contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="d9a53-146">Enumeração de fontes.</span><span class="sxs-lookup"><span data-stu-id="d9a53-146">Font enumeration.</span></span>
- <span data-ttu-id="d9a53-147">API de fonte.</span><span class="sxs-lookup"><span data-stu-id="d9a53-147">Font API.</span></span>
- <span data-ttu-id="d9a53-148">Dela.</span><span class="sxs-lookup"><span data-stu-id="d9a53-148">Shaping.</span></span>
- <span data-ttu-id="d9a53-149">APIs de renderização de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="d9a53-149">Low-level rendering APIs.</span></span> <span data-ttu-id="d9a53-150">Isso é parcial na fase atual &mdash; DWriteCore não interopera com [Direct2D](../direct2d/direct2d-portal.md), mas você pode usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d9a53-150">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="d9a53-151">Funcionalidade básica de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-151">Basic text layout functionality.</span></span>
- <span data-ttu-id="d9a53-152">APIs de renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="d9a53-152">Text-rendering APIs.</span></span>
- <span data-ttu-id="d9a53-153">Destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="d9a53-153">Bitmap render target.</span></span>
- <span data-ttu-id="d9a53-154">Fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="d9a53-154">Color fonts.</span></span>
- <span data-ttu-id="d9a53-155">Otimizações diversas (limpeza do cache de fontes, carregador de fonte em memória e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="d9a53-155">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="d9a53-156">Um recurso de faixa é fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="d9a53-156">A banner feature is color fonts.</span></span> <span data-ttu-id="d9a53-157">As fontes de cores permitem que você processe suas fontes com funcionalidade de cores mais sofisticada além das simples cores únicas.</span><span class="sxs-lookup"><span data-stu-id="d9a53-157">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="d9a53-158">Por exemplo, fontes de cor é o que capacita a capacidade de renderizar Emoji e fontes de ícone da barra de ferramentas (o último usado pelo Office, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="d9a53-158">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="d9a53-159">As fontes de cores foram introduzidas pela primeira vez no Windows 8.1, mas o recurso estava muito expandido no Windows 10, versão 1607 (atualização de aniversário).</span><span class="sxs-lookup"><span data-stu-id="d9a53-159">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="d9a53-160">O trabalho na limpeza do cache de fontes e no carregador de fontes na memória, permite o carregamento mais rápido de fontes e melhorias na memória.</span><span class="sxs-lookup"><span data-stu-id="d9a53-160">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="d9a53-161">Com esses recursos, você pode começar imediatamente a aproveitar algumas das principais funcionalidades do DirectWrite &mdash; , como fontes variáveis.</span><span class="sxs-lookup"><span data-stu-id="d9a53-161">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts.</span></span> <span data-ttu-id="d9a53-162">Fontes de variáveis são um dos recursos mais importantes para clientes do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9a53-162">Variable fonts are one of the most important features for DirectWrite customers.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="d9a53-163">Nosso convite para você como desenvolvedor DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d9a53-163">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="d9a53-164">DWriteCore, juntamente com outros componentes de reunião do projeto, serão desenvolvidos com a abertura para comentários do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="d9a53-164">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="d9a53-165">Convidamos você a começar a explorar o DWriteCore e a fornecer ideias ou solicitações ao desenvolvimento de recursos em nosso [repositório GitHub de reunião do projeto](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="d9a53-165">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="d9a53-166">Programando com DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-166">Programming with DWriteCore</span></span>

<span data-ttu-id="d9a53-167">Assim como com o [DirectWrite](./direct-write-portal.md), você programa com DWriteCore por meio de sua API com-Light, por meio da interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="d9a53-167">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="d9a53-168">Para usar o DWriteCore, é necessário incluir o `dwrite_core.h` arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d9a53-168">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="d9a53-169">O `dwrite_core.h` arquivo de cabeçalho primeiro define o token *DWRITE_CORE* e, em seguida, inclui o `dwrite_3.h` arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d9a53-169">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes the `dwrite_3.h` header file.</span></span> <span data-ttu-id="d9a53-170">O token *DWRITE_CORE* é importante, pois ele direciona quaisquer cabeçalhos incluídos subsequentemente para disponibilizar todas as APIs DirectWrite para você.</span><span class="sxs-lookup"><span data-stu-id="d9a53-170">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="d9a53-171">Depois que o projeto tiver sido incluído `dwrite_core.h` , você poderá continuar e escrever código, criar e executar.</span><span class="sxs-lookup"><span data-stu-id="d9a53-171">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="d9a53-172">APIs que são novas ou diferentes para DWriteCore</span><span class="sxs-lookup"><span data-stu-id="d9a53-172">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="d9a53-173">A superfície da API do DWriteCore é basicamente a mesma que se trata de [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="d9a53-173">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="d9a53-174">Mas há um pequeno número de novas APIs que só estão em DWriteCore no presente.</span><span class="sxs-lookup"><span data-stu-id="d9a53-174">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-factory-object"></a><span data-ttu-id="d9a53-175">Criar um objeto de fábrica</span><span class="sxs-lookup"><span data-stu-id="d9a53-175">Create a factory object</span></span>

<span data-ttu-id="d9a53-176">A função Free [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) cria um objeto de fábrica que é usado para a criação subsequente de objetos DWriteCore individuais.</span><span class="sxs-lookup"><span data-stu-id="d9a53-176">The [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

<span data-ttu-id="d9a53-177">**DWriteCoreCreateFactory** é funcionalmente o mesmo que a função [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) exportada pela versão do sistema do DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="d9a53-177">**DWriteCoreCreateFactory** is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="d9a53-178">A função DWriteCore tem um nome diferente para evitar ambigüidade.</span><span class="sxs-lookup"><span data-stu-id="d9a53-178">The DWriteCore function has a different name to avoid ambiguity.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="d9a53-179">Criar um objeto de fábrica restrito</span><span class="sxs-lookup"><span data-stu-id="d9a53-179">Create a restricted factory object</span></span>

<span data-ttu-id="d9a53-180">A enumeração de [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) tem uma nova constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indicando uma fábrica restrita.</span><span class="sxs-lookup"><span data-stu-id="d9a53-180">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="d9a53-181">Uma fábrica restrita é mais bloqueada do que uma fábrica isolada.</span><span class="sxs-lookup"><span data-stu-id="d9a53-181">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="d9a53-182">Ele não interage com um cache de fontes entre processos e persistentes de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="d9a53-182">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="d9a53-183">Além disso, a coleção de fontes do sistema retornada por essa fábrica inclui apenas fontes conhecidas.</span><span class="sxs-lookup"><span data-stu-id="d9a53-183">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="d9a53-184">Veja como você pode usar **DWRITE_FACTORY_TYPE_ISOLATED2** para criar um objeto de fábrica restrito ao chamar a função gratuita [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) .</span><span class="sxs-lookup"><span data-stu-id="d9a53-184">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](./dwrite_core/nf-dwrite_core-dwritecorecreatefactory.md) free function.</span></span>

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

<span data-ttu-id="d9a53-185">Se você passar **DWRITE_FACTORY_TYPE_ISOLATED2** para uma versão mais antiga do DirectWrite que não ofereça suporte a ela, **DWriteCreateFactory** retornará **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="d9a53-185">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="d9a53-186">Glifos de desenho para um bitmap de memória do sistema</span><span class="sxs-lookup"><span data-stu-id="d9a53-186">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="d9a53-187">DirectWrite tem uma interface de destino de renderização de bitmap que dá suporte à renderização de glifos em um bitmap na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="d9a53-187">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="d9a53-188">No entanto, atualmente a única maneira de obter acesso aos dados de pixel subjacentes é passar pelo GDI e, portanto, a API não é utilizável entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="d9a53-188">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="d9a53-189">Isso é facilmente remediado com a adição de um método para recuperar os dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="d9a53-189">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="d9a53-190">Portanto, DWriteCore apresenta a interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e seu método [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="d9a53-190">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="d9a53-191">Esse método usa um parâmetro de tipo (ponteiro para) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que é uma nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="d9a53-191">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="d9a53-192">Seu aplicativo cria um destino de renderização de bitmap chamando [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="d9a53-192">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="d9a53-193">No Windows, um destino de renderização de bitmap encapsula um controlador de domínio de memória GDI com um bitmap independente de dispositivo (DIB) do GDI selecionado.</span><span class="sxs-lookup"><span data-stu-id="d9a53-193">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="d9a53-194">[IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) processa glifos para o DIB.</span><span class="sxs-lookup"><span data-stu-id="d9a53-194">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="d9a53-195">DirectWrite renderiza os glifos em si sem passar pela GDI.</span><span class="sxs-lookup"><span data-stu-id="d9a53-195">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="d9a53-196">Em seguida, seu aplicativo pode obter o **HDC** do destino de renderização de bitmap e usar [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar os pixels para uma janela **HDC**.</span><span class="sxs-lookup"><span data-stu-id="d9a53-196">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="d9a53-197">Em plataformas não Windows, seu aplicativo ainda pode criar um destino de renderização de bitmap, mas simplesmente encapsula uma matriz de memória do sistema sem **HDC** e sem DIB.</span><span class="sxs-lookup"><span data-stu-id="d9a53-197">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="d9a53-198">Sem um **HDC**, precisa haver outra maneira de seu aplicativo obter os pixels de bitmap para que ele possa copiá-los ou usá-los de outra forma.</span><span class="sxs-lookup"><span data-stu-id="d9a53-198">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="d9a53-199">Mesmo no Windows, às vezes é útil obter os dados reais do pixel, e mostramos a maneira atual de fazer isso no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="d9a53-199">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="d9a53-200">Outras diferenças de API entre DWriteCore e DirectWrite</span><span class="sxs-lookup"><span data-stu-id="d9a53-200">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="d9a53-201">Há algumas APIs que são apenas stubs ou se comportam de forma um pouco diferente em plataformas não Windows.</span><span class="sxs-lookup"><span data-stu-id="d9a53-201">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="d9a53-202">Por exemplo, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retorna E_NOTIMPL em plataformas que não são do Windows, pois não há nenhum **HDC** sem [GDI.](../gdi/windows-gdi.md) </span><span class="sxs-lookup"><span data-stu-id="d9a53-202">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="d9a53-203">E, por fim, há determinadas outras APIs do Windows que normalmente são usadas junto com DirectWrite (Direct2D sendo um exemplo notável).</span><span class="sxs-lookup"><span data-stu-id="d9a53-203">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="d9a53-204">No entanto, atualmente, Direct2D e DWriteCore não interoperam.</span><span class="sxs-lookup"><span data-stu-id="d9a53-204">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="d9a53-205">Por exemplo, se você criar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e passá-lo para [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="d9a53-205">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
