---
title: Visão geral do DWriteCore
description: DWriteCore é a implementação de reunião do projeto de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/21/2021
ms.openlocfilehash: 27a34656ce28a65267bd098974b4df9003a80e17
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881835"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="5b984-105">Visão geral do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-105">DWriteCore overview</span></span>

<span data-ttu-id="5b984-106">DWriteCore é a implementação de [reunião do projeto](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md) (DirectWrite é a API do DirectX para renderização de texto de alta qualidade, fontes de estrutura de tópicos independentes de resolução e suporte completo a texto Unicode e layout).</span><span class="sxs-lookup"><span data-stu-id="5b984-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md) (DirectWrite is the DirectX API for high-quality text rendering, resolution-independent outline fonts, and full Unicode text and layout support).</span></span> <span data-ttu-id="5b984-107">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="5b984-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="5b984-108">Este tópico introdutório descreve o que é o DWriteCore e mostra como instalá-lo em seu ambiente de desenvolvimento e programar com ele.</span><span class="sxs-lookup"><span data-stu-id="5b984-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="5b984-109">A proposta de valor de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="5b984-110">O [DirectWrite](./direct-write-portal.md) em si dá suporte a uma ampla gama de recursos que o torna a ferramenta de renderização de fontes de escolha no Windows para a maioria dos aplicativos &mdash; , seja por meio de chamadas diretas ou por meio de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="5b984-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="5b984-111">O DirectWrite inclui um sistema de layout de texto independente de dispositivo, renderização de texto de alta qualidade de subpixel [do Microsoft ClearType](/typography/cleartype/) , texto acelerado por hardware, texto de vários formatos, recursos de tipografia de [® de OpenType](/typography/opentype/) avançados, suporte a todo o idioma e renderização e processamento compatíveis com [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="5b984-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="5b984-112">O DirectWrite está disponível desde o Windows Vista SP2 e evoluiu ao longo dos anos para incluir recursos mais avançados, como fontes variáveis, que permitem aos desenvolvedores aplicar estilos, pesos e outros atributos a uma fonte com apenas um recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="5b984-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="5b984-113">No entanto, devido à longa vida útil do DirectWrite, os avanços no desenvolvimento têm o tendiam de deixar versões anteriores do Windows atrás.</span><span class="sxs-lookup"><span data-stu-id="5b984-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="5b984-114">Além disso, o status do DirectWrite como a tecnologia de renderização de texto Premier é limitado apenas ao Windows, deixando aplicativos de plataforma cruzada para gravar sua própria pilha de renderização de texto ou para se basear em soluções de terceiros.</span><span class="sxs-lookup"><span data-stu-id="5b984-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="5b984-115">O DWriteCore resolve os problemas fundamentais de órfão de recursos de versão e compatibilidade entre plataformas removendo a biblioteca do sistema e direcionando todos os pontos de extremidade possíveis com suporte.</span><span class="sxs-lookup"><span data-stu-id="5b984-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="5b984-116">Para esse fim, integramos o DWriteCore à reunião do projeto com uma API pública que tem suporte em todos os pontos de extremidade do Windows até o Windows 8 e abre a porta para que você o use entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="5b984-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="5b984-117">O valor principal que o DWriteCore fornece a você, como desenvolvedor, na reunião do projeto, é que ele fornece acesso a todos os recursos atuais do DirectWrite, desde o nível inferior até o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5b984-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="5b984-118">Todos os recursos do DWriteCore funcionarão da mesma forma em todas as versões de nível inferior; em outras palavras, todos os recursos atuais funcionarão no Windows 8, 8,1 e em todas as versões do Windows 10, sem qualquer diferença em relação a quais recursos podem funcionar em quais versões.</span><span class="sxs-lookup"><span data-stu-id="5b984-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="5b984-119">O aplicativo de demonstração DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="5b984-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="5b984-120">O DWriteCore é demonstrado por meio do aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que está disponível para você agora para baixar e estudar.</span><span class="sxs-lookup"><span data-stu-id="5b984-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="5b984-121">Introdução ao DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-121">Get started with DWriteCore</span></span>

<span data-ttu-id="5b984-122">DWriteCore faz parte do [projeto reunião 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span><span class="sxs-lookup"><span data-stu-id="5b984-122">DWriteCore is part of [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0).</span></span> <span data-ttu-id="5b984-123">Esta seção descreve como configurar seu ambiente de desenvolvimento para a programação com o DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="5b984-123">This section describes how to set up your development environment for programming with DWriteCore.</span></span>

### <a name="install-the-project-reunion-05-vsix"></a><span data-ttu-id="5b984-124">Instalar o VSIX do projeto reunião 0,5</span><span class="sxs-lookup"><span data-stu-id="5b984-124">Install the Project Reunion 0.5 VSIX</span></span>

<span data-ttu-id="5b984-125">No Visual Studio, clique em **extensões**  >  **gerenciar extensões**, pesquise por *reunião do projeto* e baixe a extensão de reunião do projeto.</span><span class="sxs-lookup"><span data-stu-id="5b984-125">In Visual Studio, click **Extensions** > **Manage Extensions**, search for *Project Reunion*, and download the Project Reunion extension.</span></span> <span data-ttu-id="5b984-126">Feche e reabra o Visual Studio e siga os prompts para instalar a extensão.</span><span class="sxs-lookup"><span data-stu-id="5b984-126">Close and reopen Visual Studio, and follow the prompts to install the extension.</span></span>

<span data-ttu-id="5b984-127">Para obter mais informações, consulte [reunião do projeto 0,5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)e [criar aplicativos do Windows para desktop com a reunião do projeto 0,5](/windows/apps/project-reunion/#set-up-your-development-environment).</span><span class="sxs-lookup"><span data-stu-id="5b984-127">For more info, see [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0), and [Build desktop Windows apps with Project Reunion 0.5](/windows/apps/project-reunion/#set-up-your-development-environment).</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="5b984-128">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="5b984-128">Create a new project</span></span>

<span data-ttu-id="5b984-129">No Visual Studio, crie um novo projeto do modelo de projeto **aplicativo em branco, empacotado (WinUI 3 no desktop)** .</span><span class="sxs-lookup"><span data-stu-id="5b984-129">In Visual Studio, create a new project from the **Blank App, Packaged (WinUI 3 in Desktop)** project template.</span></span> <span data-ttu-id="5b984-130">Você pode encontrar esse modelo de projeto escolhendo linguagem: *C++*; plataforma: *reunião do projeto*; tipo de projeto: *área de trabalho*.</span><span class="sxs-lookup"><span data-stu-id="5b984-130">You can find that project template by choosing language: *C++*; platform: *Project Reunion*; project type: *Desktop*.</span></span>

<span data-ttu-id="5b984-131">Para obter mais informações, consulte [modelos de projeto para WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span><span class="sxs-lookup"><span data-stu-id="5b984-131">For more info, see [Project templates for WinUI 3](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3).</span></span>

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a><span data-ttu-id="5b984-132">Instalar o pacote NuGet Microsoft. ProjectReunion. DWrite</span><span class="sxs-lookup"><span data-stu-id="5b984-132">Install the Microsoft.ProjectReunion.DWrite NuGet package</span></span>

<span data-ttu-id="5b984-133">No Visual Studio, clique em **projeto** \> **gerenciar pacotes NuGet...** \> **procure**, digite ou cole **Microsoft. ProjectReunion. DWrite** na caixa de pesquisa, selecione o item nos resultados da pesquisa e clique em **instalar** para instalar o pacote para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="5b984-133">In Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.ProjectReunion.DWrite** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a><span data-ttu-id="5b984-134">Como alternativa, comece com o aplicativo de exemplo DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="5b984-134">Alternatively, begin with the DWriteCoreGallery sample app</span></span>

<span data-ttu-id="5b984-135">Como alternativa, você pode programar com DWriteCore começando com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basear seu desenvolvimento nesse projeto.</span><span class="sxs-lookup"><span data-stu-id="5b984-135">Alternatively, you can program with DWriteCore by beginning with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span> <span data-ttu-id="5b984-136">Você pode, então, ficar à vontade para remover qualquer código-fonte (ou arquivos) existente desse projeto de exemplo e adicionar qualquer código-fonte (ou arquivos) novo ao projeto.</span><span class="sxs-lookup"><span data-stu-id="5b984-136">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span>

### <a name="use-dwritecore-in-your-project"></a><span data-ttu-id="5b984-137">Usar o DWriteCore em seu projeto</span><span class="sxs-lookup"><span data-stu-id="5b984-137">Use DWriteCore in your project</span></span>

<span data-ttu-id="5b984-138">Para obter mais informações sobre programação com o DWriteCore, consulte a seção [programação com DWriteCore](#programming-with-dwritecore) mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="5b984-138">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="5b984-139">As fases de lançamento do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-139">The release phases of DWriteCore</span></span>

<span data-ttu-id="5b984-140">Portar DirectWrite para DWriteCore é um projeto suficientemente grande para abranger vários ciclos de versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="5b984-140">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="5b984-141">Esse projeto é dividido em fases, cada uma correspondendo a uma parte da funcionalidade fornecida em uma versão.</span><span class="sxs-lookup"><span data-stu-id="5b984-141">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="5b984-142">Recursos na versão atual do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-142">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="5b984-143">A versão do DWriteCore atualmente disponível contém as ferramentas básicas que você, como desenvolvedor, precisa consumir o DWriteCore, incluindo os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b984-143">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="5b984-144">Enumeração de fontes.</span><span class="sxs-lookup"><span data-stu-id="5b984-144">Font enumeration.</span></span>
- <span data-ttu-id="5b984-145">API de fonte.</span><span class="sxs-lookup"><span data-stu-id="5b984-145">Font API.</span></span>
- <span data-ttu-id="5b984-146">Dela.</span><span class="sxs-lookup"><span data-stu-id="5b984-146">Shaping.</span></span>
- <span data-ttu-id="5b984-147">APIs de renderização de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="5b984-147">Low-level rendering APIs.</span></span> <span data-ttu-id="5b984-148">Isso é parcial na fase atual &mdash; DWriteCore não interopera com [Direct2D](../direct2d/direct2d-portal.md), mas você pode usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="5b984-148">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="5b984-149">Funcionalidade básica de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="5b984-149">Basic text layout functionality.</span></span>
- <span data-ttu-id="5b984-150">APIs de renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="5b984-150">Text-rendering APIs.</span></span>
- <span data-ttu-id="5b984-151">Destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="5b984-151">Bitmap render target.</span></span>
- <span data-ttu-id="5b984-152">Fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="5b984-152">Color fonts.</span></span>
- <span data-ttu-id="5b984-153">Otimizações diversas (limpeza do cache de fontes, carregador de fonte em memória e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="5b984-153">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="5b984-154">O recurso de faixa neste estágio é fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="5b984-154">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="5b984-155">As fontes de cores permitem que você processe suas fontes com funcionalidade de cores mais sofisticada além das simples cores únicas.</span><span class="sxs-lookup"><span data-stu-id="5b984-155">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="5b984-156">Por exemplo, fontes de cor é o que capacita a capacidade de renderizar Emoji e fontes de ícone da barra de ferramentas (o último usado pelo Office, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="5b984-156">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="5b984-157">As fontes de cores foram introduzidas pela primeira vez no Windows 8.1, mas o recurso estava muito expandido no Windows 10, versão 1607 (atualização de aniversário).</span><span class="sxs-lookup"><span data-stu-id="5b984-157">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="5b984-158">O trabalho na limpeza do cache de fontes e no carregador de fontes na memória, permite o carregamento mais rápido de fontes e melhorias na memória.</span><span class="sxs-lookup"><span data-stu-id="5b984-158">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="5b984-159">Com esses recursos, você pode começar imediatamente a aproveitar algumas das principais funcionalidades do DirectWrite &mdash; , como fontes variáveis de &mdash; nível inferior para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5b984-159">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="5b984-160">Essa iteração da biblioteca também pode ser consumida no [Android](https://www.android.com/)e no **Linux**.</span><span class="sxs-lookup"><span data-stu-id="5b984-160">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="5b984-161">Fontes de variáveis são um dos recursos mais importantes para clientes do DirectWrite; Eles foram introduzidos no Windows 10, versão 1709 (atualização para criadores de outono), portanto, acessá-los em versões anteriores é um grande benefício para você como desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="5b984-161">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="5b984-162">Nosso convite para você como desenvolvedor DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5b984-162">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="5b984-163">DWriteCore, juntamente com outros componentes de reunião do projeto, serão desenvolvidos com a abertura para comentários do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="5b984-163">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="5b984-164">Convidamos você a começar a explorar o DWriteCore e a fornecer ideias ou solicitações ao desenvolvimento de recursos em nosso [repositório GitHub de reunião do projeto](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="5b984-164">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="5b984-165">Programando com DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-165">Programming with DWriteCore</span></span>

<span data-ttu-id="5b984-166">Assim como com o [DirectWrite](./direct-write-portal.md), você programa com DWriteCore por meio de sua API com-Light, por meio da interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="5b984-166">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="5b984-167">Para usar o DWriteCore, é necessário incluir o `dwrite_core.h` arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="5b984-167">To use DWriteCore, it's necessary to include the `dwrite_core.h` header file.</span></span>

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

<span data-ttu-id="5b984-168">O `dwrite_core.h` arquivo de cabeçalho primeiro define o token *DWRITE_CORE* e, em seguida, inclui `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="5b984-168">The `dwrite_core.h` header file first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="5b984-169">O token *DWRITE_CORE* é importante, pois ele direciona quaisquer cabeçalhos incluídos subsequentemente para disponibilizar todas as APIs DirectWrite para você.</span><span class="sxs-lookup"><span data-stu-id="5b984-169">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="5b984-170">Depois que o projeto tiver sido incluído `dwrite_core.h` , você poderá continuar e escrever código, criar e executar.</span><span class="sxs-lookup"><span data-stu-id="5b984-170">Once your project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="5b984-171">APIs que são novas ou diferentes para DWriteCore</span><span class="sxs-lookup"><span data-stu-id="5b984-171">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="5b984-172">A superfície da API do DWriteCore é basicamente a mesma que se trata de [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="5b984-172">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="5b984-173">Mas há um pequeno número de novas APIs que só estão em DWriteCore no presente.</span><span class="sxs-lookup"><span data-stu-id="5b984-173">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="5b984-174">Criar um objeto de fábrica restrito</span><span class="sxs-lookup"><span data-stu-id="5b984-174">Create a restricted factory object</span></span>

<span data-ttu-id="5b984-175">A enumeração de [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) tem uma nova constante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, indicando uma fábrica restrita.</span><span class="sxs-lookup"><span data-stu-id="5b984-175">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_ISOLATED2**, indicating a restricted factory.</span></span> <span data-ttu-id="5b984-176">Uma fábrica restrita é mais bloqueada do que uma fábrica isolada.</span><span class="sxs-lookup"><span data-stu-id="5b984-176">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="5b984-177">Ele não interage com um cache de fontes entre processos e persistentes de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="5b984-177">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="5b984-178">Além disso, a coleção de fontes do sistema retornada por essa fábrica inclui apenas fontes conhecidas.</span><span class="sxs-lookup"><span data-stu-id="5b984-178">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="5b984-179">Veja como você pode usar **DWRITE_FACTORY_TYPE_ISOLATED2** para criar um objeto de fábrica restrito ao chamar a função gratuita [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="5b984-179">Here's how you can use **DWRITE_FACTORY_TYPE_ISOLATED2** to create a restricted factory object when you call the [**DWriteCoreCreateFactory**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) free function.</span></span>

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

<span data-ttu-id="5b984-180">Se você passar **DWRITE_FACTORY_TYPE_ISOLATED2** para uma versão mais antiga do DirectWrite que não ofereça suporte a ela, **DWriteCreateFactory** retornará **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="5b984-180">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="5b984-181">Glifos de desenho para um bitmap de memória do sistema</span><span class="sxs-lookup"><span data-stu-id="5b984-181">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="5b984-182">DirectWrite tem uma interface de destino de renderização de bitmap que dá suporte à renderização de glifos em um bitmap na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="5b984-182">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="5b984-183">No entanto, atualmente a única maneira de obter acesso aos dados de pixel subjacentes é passar pelo GDI e, portanto, a API não é utilizável entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="5b984-183">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="5b984-184">Isso é facilmente remediado com a adição de um método para recuperar os dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="5b984-184">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="5b984-185">Portanto, DWriteCore apresenta a interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e seu método [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="5b984-185">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="5b984-186">Esse método usa um parâmetro de tipo (ponteiro para) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que é uma nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="5b984-186">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="5b984-187">Seu aplicativo cria um destino de renderização de bitmap chamando [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="5b984-187">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="5b984-188">No Windows, um destino de renderização de bitmap encapsula um controlador de domínio de memória GDI com um bitmap independente de dispositivo (DIB) do GDI selecionado.</span><span class="sxs-lookup"><span data-stu-id="5b984-188">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="5b984-189">[IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) processa glifos para o DIB.</span><span class="sxs-lookup"><span data-stu-id="5b984-189">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="5b984-190">DirectWrite renderiza os glifos em si sem passar pela GDI.</span><span class="sxs-lookup"><span data-stu-id="5b984-190">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="5b984-191">Em seguida, seu aplicativo pode obter o **HDC** do destino de renderização de bitmap e usar [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar os pixels para uma janela **HDC**.</span><span class="sxs-lookup"><span data-stu-id="5b984-191">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="5b984-192">Em plataformas não Windows, seu aplicativo ainda pode criar um destino de renderização de bitmap, mas simplesmente encapsula uma matriz de memória do sistema sem **HDC** e sem DIB.</span><span class="sxs-lookup"><span data-stu-id="5b984-192">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="5b984-193">Sem um **HDC**, precisa haver outra maneira de seu aplicativo obter os pixels de bitmap para que ele possa copiá-los ou usá-los de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5b984-193">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="5b984-194">Mesmo no Windows, às vezes é útil obter os dados reais do pixel, e mostramos a maneira atual de fazer isso no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="5b984-194">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="5b984-195">Outras diferenças de API entre DWriteCore e DirectWrite</span><span class="sxs-lookup"><span data-stu-id="5b984-195">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="5b984-196">Há algumas APIs que são apenas stubs ou que se comportam de maneira um pouco diferente em plataformas que não são do Windows.</span><span class="sxs-lookup"><span data-stu-id="5b984-196">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="5b984-197">Por exemplo, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retorna **E_NOTIMPL** em plataformas não Windows, já que não há tal coisa como um **HDC** sem [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="5b984-197">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="5b984-198">E, finalmente, existem algumas outras APIs do Windows que normalmente são usadas junto com DirectWrite (Direct2D sendo um exemplo notável).</span><span class="sxs-lookup"><span data-stu-id="5b984-198">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="5b984-199">No entanto, atualmente, Direct2D e DWriteCore não interoperam.</span><span class="sxs-lookup"><span data-stu-id="5b984-199">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="5b984-200">Por exemplo, se você criar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e passá-lo para [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="5b984-200">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>
