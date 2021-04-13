---
title: Visão geral do DWriteCore
description: DWriteCore é a implementação de reunião do projeto de DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104297856"
---
# <a name="dwritecore-overview"></a><span data-ttu-id="216f3-105">Visão geral do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-105">DWriteCore overview</span></span>

<span data-ttu-id="216f3-106">DWriteCore é a implementação de [reunião do projeto](/windows/apps/project-reunion/) de [DirectWrite](./direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="216f3-106">DWriteCore is the [Project Reunion](/windows/apps/project-reunion/) implementation of [DirectWrite](./direct-write-portal.md).</span></span> <span data-ttu-id="216f3-107">O DWriteCore é um tipo de DirectWrite que é executado em versões do Windows até o Windows 8 e permite o uso em multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="216f3-107">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="216f3-108">Este tópico introdutório descreve o que é o DWriteCore e mostra como instalá-lo em seu ambiente de desenvolvimento e programar com ele.</span><span class="sxs-lookup"><span data-stu-id="216f3-108">This introductory topic describes what DWriteCore is, and shows how to install it into your dev environment and program with it.</span></span>

## <a name="the-value-proposition-of-dwritecore"></a><span data-ttu-id="216f3-109">A proposta de valor de DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-109">The value proposition of DWriteCore</span></span>

<span data-ttu-id="216f3-110">O [DirectWrite](./direct-write-portal.md) em si dá suporte a uma ampla gama de recursos que o torna a ferramenta de renderização de fontes de escolha no Windows para a maioria dos aplicativos &mdash; , seja por meio de chamadas diretas ou por meio de [Direct2D](../direct2d/direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="216f3-110">[DirectWrite](./direct-write-portal.md) itself supports a rich array of features that makes it the font-rendering tool of choice on Windows for most apps&mdash;whether that's through direct calls, or via [Direct2D](../direct2d/direct2d-portal.md).</span></span> <span data-ttu-id="216f3-111">O DirectWrite inclui um sistema de layout de texto independente de dispositivo, renderização de texto de alta qualidade de subpixel [do Microsoft ClearType](/typography/cleartype/) , texto acelerado por hardware, texto de vários formatos, recursos de tipografia de [® de OpenType](/typography/opentype/) avançados, suporte a todo o idioma e renderização e processamento compatíveis com [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="216f3-111">DirectWrite includes a device-independent text layout system, high quality sub-pixel [Microsoft ClearType](/typography/cleartype/) text rendering, hardware-accelerated text, multi-format text, advanced [OpenType®](/typography/opentype/) typography features, wide language support, and [GDI](../gdi/windows-gdi.md)-compatible layout and rendering.</span></span> <span data-ttu-id="216f3-112">O DirectWrite está disponível desde o Windows Vista SP2 e evoluiu ao longo dos anos para incluir recursos mais avançados, como fontes variáveis, que permitem aos desenvolvedores aplicar estilos, pesos e outros atributos a uma fonte com apenas um recurso de fonte.</span><span class="sxs-lookup"><span data-stu-id="216f3-112">DirectWrite has been available since Windows Vista SP2, and it has evolved over the years to include more advanced features such as variable fonts, which enables developers to apply styles, weights, and other attributes to a font with only one font resource.</span></span>

<span data-ttu-id="216f3-113">No entanto, devido à longa vida útil do DirectWrite, os avanços no desenvolvimento têm o tendiam de deixar versões anteriores do Windows atrás.</span><span class="sxs-lookup"><span data-stu-id="216f3-113">Due to the long lifespan of DirectWrite, however, advances in development have tended to leave older versions of Windows behind.</span></span> <span data-ttu-id="216f3-114">Além disso, o status do DirectWrite como a tecnologia de renderização de texto Premier é limitado apenas ao Windows, deixando aplicativos de plataforma cruzada para gravar sua própria pilha de renderização de texto ou para se basear em soluções de terceiros.</span><span class="sxs-lookup"><span data-stu-id="216f3-114">In addition, DirectWrite's status as the premier text rendering technology is limited only to Windows, leaving cross-platform applications to either write their own text-rendering stack, or to rely on 3rd-party solutions.</span></span>

<span data-ttu-id="216f3-115">O DWriteCore resolve os problemas fundamentais de órfão de recursos de versão e compatibilidade entre plataformas removendo a biblioteca do sistema e direcionando todos os pontos de extremidade possíveis com suporte.</span><span class="sxs-lookup"><span data-stu-id="216f3-115">DWriteCore solves the fundamental problems of version feature orphaning and cross-platform compatibility by removing the library from the system, and targeting all possible supported endpoints.</span></span> <span data-ttu-id="216f3-116">Para esse fim, integramos o DWriteCore à reunião do projeto com uma API pública que tem suporte em todos os pontos de extremidade do Windows até o Windows 8 e abre a porta para que você o use entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="216f3-116">To that end, we've integrated DWriteCore into Project Reunion with a public API that's supported on all Windows endpoints down to Windows 8, and opens the door for you to use it cross-platform.</span></span>

<span data-ttu-id="216f3-117">O valor principal que o DWriteCore fornece a você, como desenvolvedor, na reunião do projeto, é que ele fornece acesso a todos os recursos atuais do DirectWrite, desde o nível inferior até o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="216f3-117">The primary value that DWriteCore gives you, as a developer, in Project Reunion is that it provides access to all current DirectWrite features all the way down-level to Windows 8.</span></span> <span data-ttu-id="216f3-118">Todos os recursos do DWriteCore funcionarão da mesma forma em todas as versões de nível inferior; em outras palavras, todos os recursos atuais funcionarão no Windows 8, 8,1 e em todas as versões do Windows 10, sem qualquer diferença em relação a quais recursos podem funcionar em quais versões.</span><span class="sxs-lookup"><span data-stu-id="216f3-118">All features of DWriteCore will function the same on all down-level versions; in other words, all current features will work on Windows 8, 8.1, and all versions of Windows 10, without any disparity regarding which features might work on which versions.</span></span>

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a><span data-ttu-id="216f3-119">O aplicativo de demonstração DWriteCore &mdash; DWriteCoreGallery</span><span class="sxs-lookup"><span data-stu-id="216f3-119">The DWriteCore demo app&mdash;DWriteCoreGallery</span></span>

<span data-ttu-id="216f3-120">O DWriteCore é demonstrado por meio do aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) , que está disponível para você agora para baixar e estudar.</span><span class="sxs-lookup"><span data-stu-id="216f3-120">DWriteCore is demonstrated by way of the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app, which is available for you now to download and study.</span></span>

## <a name="get-started-with-dwritecore"></a><span data-ttu-id="216f3-121">Introdução ao DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-121">Get started with DWriteCore</span></span>

<span data-ttu-id="216f3-122">Para o projeto de pré-lançamento da reunião 0,1, atualmente não damos suporte à instalação do pacote NuGet da reunião do projeto em seus próprios projetos.</span><span class="sxs-lookup"><span data-stu-id="216f3-122">For the Project Reunion 0.1 Prerelease, we currently don't support installing the Project Reunion NuGet package into your own projects.</span></span> <span data-ttu-id="216f3-123">Em vez disso, a opção com suporte no momento para sua própria programação com DWriteCore é começar com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) e basear seu desenvolvimento nesse projeto.</span><span class="sxs-lookup"><span data-stu-id="216f3-123">Instead, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project, and base your development on that project.</span></span>

<span data-ttu-id="216f3-124">Você pode, então, ficar à vontade para remover qualquer código-fonte (ou arquivos) existente desse projeto de exemplo e adicionar qualquer código-fonte (ou arquivos) novo ao projeto.</span><span class="sxs-lookup"><span data-stu-id="216f3-124">You can then feel free to remove any existing source code (or files) from that sample project, and to add any new source code (or files) to the project.</span></span> <span data-ttu-id="216f3-125">Para obter mais informações sobre programação com o DWriteCore, consulte a seção [programação com DWriteCore](#programming-with-dwritecore) mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="216f3-125">For more info about programming with DWriteCore, see the [Programming with DWriteCore](#programming-with-dwritecore) section later in this topic.</span></span>

## <a name="the-release-phases-of-dwritecore"></a><span data-ttu-id="216f3-126">As fases de lançamento do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-126">The release phases of DWriteCore</span></span>

<span data-ttu-id="216f3-127">Portar DirectWrite para DWriteCore é um projeto suficientemente grande para abranger vários ciclos de versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="216f3-127">Porting DirectWrite to DWriteCore is a sufficiently large project to span multiple Windows release cycles.</span></span> <span data-ttu-id="216f3-128">Esse projeto é dividido em fases, cada uma correspondendo a uma parte da funcionalidade fornecida em uma versão.</span><span class="sxs-lookup"><span data-stu-id="216f3-128">That project is divided into phases, each of which corresponds to a chunk of functionality delivered in a release.</span></span>

### <a name="features-in-the-current-release-of-dwritecore"></a><span data-ttu-id="216f3-129">Recursos na versão atual do DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-129">Features in the current release of DWriteCore</span></span>

<span data-ttu-id="216f3-130">A versão do DWriteCore atualmente disponível contém as ferramentas básicas que você, como desenvolvedor, precisa consumir o DWriteCore, incluindo os recursos a seguir.</span><span class="sxs-lookup"><span data-stu-id="216f3-130">The version of DWriteCore currently available contains the basic tools that you, as a developer, need to consume DWriteCore, including the following features.</span></span>

- <span data-ttu-id="216f3-131">Enumeração de fontes.</span><span class="sxs-lookup"><span data-stu-id="216f3-131">Font enumeration.</span></span>
- <span data-ttu-id="216f3-132">API de fonte.</span><span class="sxs-lookup"><span data-stu-id="216f3-132">Font API.</span></span>
- <span data-ttu-id="216f3-133">Dela.</span><span class="sxs-lookup"><span data-stu-id="216f3-133">Shaping.</span></span>
- <span data-ttu-id="216f3-134">APIs de renderização de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="216f3-134">Low-level rendering APIs.</span></span> <span data-ttu-id="216f3-135">Isso é parcial na fase atual &mdash; DWriteCore não interopera com [Direct2D](../direct2d/direct2d-portal.md), mas você pode usar [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) e [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="216f3-135">This is partial at the current phase&mdash;DWriteCore doesn't interoperate with [Direct2D](../direct2d/direct2d-portal.md), but you can use [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) and [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget).</span></span>
- <span data-ttu-id="216f3-136">Funcionalidade básica de layout de texto.</span><span class="sxs-lookup"><span data-stu-id="216f3-136">Basic text layout functionality.</span></span>
- <span data-ttu-id="216f3-137">APIs de renderização de texto.</span><span class="sxs-lookup"><span data-stu-id="216f3-137">Text-rendering APIs.</span></span>
- <span data-ttu-id="216f3-138">Destino de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="216f3-138">Bitmap render target.</span></span>
- <span data-ttu-id="216f3-139">Fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="216f3-139">Color fonts.</span></span>
- <span data-ttu-id="216f3-140">Otimizações diversas (limpeza do cache de fontes, carregador de fonte em memória e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="216f3-140">Miscellaneous optimizations (font cache cleanup, in-memory font loader, and so on).</span></span>

<span data-ttu-id="216f3-141">O recurso de faixa neste estágio é fontes de cores.</span><span class="sxs-lookup"><span data-stu-id="216f3-141">The banner feature at this stage is color fonts.</span></span> <span data-ttu-id="216f3-142">As fontes de cores permitem que você processe suas fontes com funcionalidade de cores mais sofisticada além das simples cores únicas.</span><span class="sxs-lookup"><span data-stu-id="216f3-142">Color fonts enable you to render your fonts with more sophisticated color functionality beyond simple single colors.</span></span> <span data-ttu-id="216f3-143">Por exemplo, fontes de cor é o que capacita a capacidade de renderizar Emoji e fontes de ícone da barra de ferramentas (o último usado pelo Office, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="216f3-143">For example, color fonts is what powers the ability to render emoji and toolbar icon fonts (the latter of which is used by Office, for example).</span></span> <span data-ttu-id="216f3-144">As fontes de cores foram introduzidas pela primeira vez no Windows 8.1, mas o recurso estava muito expandido no Windows 10, versão 1607 (atualização de aniversário).</span><span class="sxs-lookup"><span data-stu-id="216f3-144">Color fonts were first introduced in Windows 8.1, but the feature was heavily expanded upon in Windows 10, version 1607 (Anniversary Update).</span></span>

<span data-ttu-id="216f3-145">O trabalho na limpeza do cache de fontes e no carregador de fontes na memória, permite o carregamento mais rápido de fontes e melhorias na memória.</span><span class="sxs-lookup"><span data-stu-id="216f3-145">The work on cleanup of the font cache, and the in-memory font loader, allow for faster loading of fonts, and memory improvements.</span></span>

<span data-ttu-id="216f3-146">Com esses recursos, você pode começar imediatamente a aproveitar algumas das principais funcionalidades do DirectWrite &mdash; , como fontes variáveis de &mdash; nível inferior para o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="216f3-146">With these features, you can immediately begin to harness some of DirectWrite's modern core functionality&mdash;such as variable fonts&mdash;down-level to Windows 8.</span></span> <span data-ttu-id="216f3-147">Essa iteração da biblioteca também pode ser consumida no [Android](https://www.android.com/)e no **Linux**.</span><span class="sxs-lookup"><span data-stu-id="216f3-147">This iteration of the library can also be consumed on [Android](https://www.android.com/), and **Linux**.</span></span> <span data-ttu-id="216f3-148">Fontes de variáveis são um dos recursos mais importantes para clientes do DirectWrite; Eles foram introduzidos no Windows 10, versão 1709 (atualização para criadores de outono), portanto, acessá-los em versões anteriores é um grande benefício para você como desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="216f3-148">Variable fonts are one of the most important features for DirectWrite customers; they were introduced in Windows 10, version 1709 (Fall Creators Update), so accessing them in previous versions is a massive boon to you as a developer.</span></span>

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a><span data-ttu-id="216f3-149">Nosso convite para você como desenvolvedor DirectWrite</span><span class="sxs-lookup"><span data-stu-id="216f3-149">Our invitation to you as a DirectWrite developer</span></span>

<span data-ttu-id="216f3-150">DWriteCore, juntamente com outros componentes de reunião do projeto, serão desenvolvidos com a abertura para comentários do desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="216f3-150">DWriteCore, along with other Project Reunion components, will be developed with openness to developer feedback.</span></span> <span data-ttu-id="216f3-151">Convidamos você a começar a explorar o DWriteCore e a fornecer ideias ou solicitações ao desenvolvimento de recursos em nosso [repositório GitHub de reunião do projeto](https://github.com/microsoft/ProjectReunion/).</span><span class="sxs-lookup"><span data-stu-id="216f3-151">We invite you to begin exploring DWriteCore, and to provide insights or requests into feature development on our [Project Reunion GitHub repository](https://github.com/microsoft/ProjectReunion/).</span></span>

## <a name="programming-with-dwritecore"></a><span data-ttu-id="216f3-152">Programando com DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-152">Programming with DWriteCore</span></span>

<span data-ttu-id="216f3-153">Como já mencionado, para o projeto de pré-lançamento da reunião 0,1, a opção com suporte no momento para sua própria programação com DWriteCore é começar com o projeto de aplicativo de exemplo [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="216f3-153">As already mentioned, for the Project Reunion 0.1 Prerelease, the currently supported option for your own programming with DWriteCore is to begin with the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app project.</span></span>

<span data-ttu-id="216f3-154">Assim como com o [DirectWrite](./direct-write-portal.md), você programa com DWriteCore por meio de sua API com-Light, por meio da interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) .</span><span class="sxs-lookup"><span data-stu-id="216f3-154">Just like with [DirectWrite](./direct-write-portal.md), you program with DWriteCore via its COM-light API, through the [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) interface.</span></span>

<span data-ttu-id="216f3-155">**DWriteCoreGallery** já inclui o `dwrite_core.h` arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="216f3-155">**DWriteCoreGallery** already includes the `dwrite_core.h` header file.</span></span> <span data-ttu-id="216f3-156">Esse cabeçalho define primeiro o token *DWRITE_CORE* e, em seguida, inclui `dwrite_3.h` .</span><span class="sxs-lookup"><span data-stu-id="216f3-156">That header first defines the token *DWRITE_CORE*, and then it includes `dwrite_3.h`.</span></span> <span data-ttu-id="216f3-157">O token *DWRITE_CORE* é importante, pois ele direciona quaisquer cabeçalhos incluídos subsequentemente para disponibilizar todas as APIs DirectWrite para você.</span><span class="sxs-lookup"><span data-stu-id="216f3-157">The *DWRITE_CORE* token is important, because it directs any subsequently included headers to make all of the DirectWrite APIs available to you.</span></span> <span data-ttu-id="216f3-158">Depois que um projeto é incluído `dwrite_core.h` , você pode continuar e escrever código, criar e executar.</span><span class="sxs-lookup"><span data-stu-id="216f3-158">Once a project has included `dwrite_core.h`, you can then go ahead and write code, build, and run.</span></span>

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a><span data-ttu-id="216f3-159">APIs que são novas ou diferentes para DWriteCore</span><span class="sxs-lookup"><span data-stu-id="216f3-159">APIs that are new, or different, for DWriteCore</span></span>

<span data-ttu-id="216f3-160">A superfície da API do DWriteCore é basicamente a mesma que se trata de [DirectWrite](/windows/win32/api/_directwrite/).</span><span class="sxs-lookup"><span data-stu-id="216f3-160">The DWriteCore API surface is the largely the same as it is for [DirectWrite](/windows/win32/api/_directwrite/).</span></span> <span data-ttu-id="216f3-161">Mas há um pequeno número de novas APIs que só estão em DWriteCore no presente.</span><span class="sxs-lookup"><span data-stu-id="216f3-161">But there are a small number of new APIs that are only in DWriteCore at the present.</span></span>

#### <a name="create-a-restricted-factory-object"></a><span data-ttu-id="216f3-162">Criar um objeto de fábrica restrito</span><span class="sxs-lookup"><span data-stu-id="216f3-162">Create a restricted factory object</span></span>

<span data-ttu-id="216f3-163">A enumeração de [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) tem uma nova constante &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**.</span><span class="sxs-lookup"><span data-stu-id="216f3-163">The [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) enumeration has a new constant&mdash;**DWRITE_FACTORY_TYPE_RESTRICTED**.</span></span> <span data-ttu-id="216f3-164">Uma fábrica restrita é mais bloqueada do que uma fábrica isolada.</span><span class="sxs-lookup"><span data-stu-id="216f3-164">A restricted factory is more locked-down than an isolated factory.</span></span> <span data-ttu-id="216f3-165">Ele não interage com um cache de fontes entre processos e persistentes de nenhuma forma.</span><span class="sxs-lookup"><span data-stu-id="216f3-165">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="216f3-166">Além disso, a coleção de fontes do sistema retornada por essa fábrica inclui apenas fontes conhecidas.</span><span class="sxs-lookup"><span data-stu-id="216f3-166">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="216f3-167">Veja como você pode usar **DWRITE_FACTORY_TYPE_RESTRICTED** para criar um objeto de fábrica restrito ao chamar a função gratuita [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) .</span><span class="sxs-lookup"><span data-stu-id="216f3-167">Here's how you can use **DWRITE_FACTORY_TYPE_RESTRICTED** to create a restricted factory object when you call the [**DWriteCreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) free function.</span></span>

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

<span data-ttu-id="216f3-168">Se você passar **DWRITE_FACTORY_TYPE_RESTRICTED** para uma versão mais antiga do DirectWrite que não ofereça suporte a ela, **DWriteCreateFactory** retornará **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="216f3-168">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to an older version of DirectWrite that doesn't support it, then **DWriteCreateFactory** returns **E_INVALIDARG**.</span></span>

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a><span data-ttu-id="216f3-169">Glifos de desenho para um bitmap de memória do sistema</span><span class="sxs-lookup"><span data-stu-id="216f3-169">Drawing glyphs to a system memory bitmap</span></span>

<span data-ttu-id="216f3-170">DirectWrite tem uma interface de destino de renderização de bitmap que dá suporte à renderização de glifos em um bitmap na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="216f3-170">DirectWrite has a bitmap render target interface that supports rendering glyphs to a bitmap in system memory.</span></span> <span data-ttu-id="216f3-171">No entanto, atualmente a única maneira de obter acesso aos dados de pixel subjacentes é passar pelo GDI e, portanto, a API não é utilizável entre plataformas.</span><span class="sxs-lookup"><span data-stu-id="216f3-171">However, currently the only way to get access to the underlying pixel data is to go through GDI, and so the API is not usable cross-platform.</span></span> <span data-ttu-id="216f3-172">Isso é facilmente remediado com a adição de um método para recuperar os dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="216f3-172">This is easily remedied by adding a method to retrieve the pixel data.</span></span>

<span data-ttu-id="216f3-173">Portanto, DWriteCore apresenta a interface [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) e seu método [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span><span class="sxs-lookup"><span data-stu-id="216f3-173">And so DWriteCore introduces the [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) interface, and its method [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md).</span></span> <span data-ttu-id="216f3-174">Esse método usa um parâmetro de tipo (ponteiro para) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), que é uma nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="216f3-174">That method takes a parameter of (pointer to) type [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), which is a new struct.</span></span>

<span data-ttu-id="216f3-175">Seu aplicativo cria um destino de renderização de bitmap chamando [IDWriteGdiInterop:: CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span><span class="sxs-lookup"><span data-stu-id="216f3-175">Your application creates a bitmap render target by calling [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget).</span></span> <span data-ttu-id="216f3-176">No Windows, um destino de renderização de bitmap encapsula um controlador de domínio de memória GDI com um bitmap independente de dispositivo (DIB) do GDI selecionado.</span><span class="sxs-lookup"><span data-stu-id="216f3-176">On Windows, a bitmap render target encapsulates a GDI memory DC with a GDI device-independent bitmap (DIB) selected into it.</span></span> <span data-ttu-id="216f3-177">[IDWriteBitmapRenderTarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) processa glifos para o DIB.</span><span class="sxs-lookup"><span data-stu-id="216f3-177">[IDWriteBitmapRenderTarget::DrawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) renders glyphs to the DIB.</span></span> <span data-ttu-id="216f3-178">DirectWrite renderiza os glifos em si sem passar pela GDI.</span><span class="sxs-lookup"><span data-stu-id="216f3-178">DirectWrite renders the glyphs itself without going through GDI.</span></span> <span data-ttu-id="216f3-179">Em seguida, seu aplicativo pode obter o **HDC** do destino de renderização de bitmap e usar [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) para copiar os pixels para uma janela **HDC**.</span><span class="sxs-lookup"><span data-stu-id="216f3-179">Your application can then get the **HDC** from the bitmap render target, and use [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) to copy the pixels to a window **HDC**.</span></span>

<span data-ttu-id="216f3-180">Em plataformas não Windows, seu aplicativo ainda pode criar um destino de renderização de bitmap, mas simplesmente encapsula uma matriz de memória do sistema sem **HDC** e sem DIB.</span><span class="sxs-lookup"><span data-stu-id="216f3-180">On non-Windows platforms, your application can still create a bitmap render target, but it simply encapsulates a system memory array with no **HDC** and no DIB.</span></span> <span data-ttu-id="216f3-181">Sem um **HDC**, precisa haver outra maneira de seu aplicativo obter os pixels de bitmap para que ele possa copiá-los ou usá-los de outra forma.</span><span class="sxs-lookup"><span data-stu-id="216f3-181">Without an **HDC**, there needs to be another way for your application to get the bitmap pixels so that it can copy them, or otherwise use them.</span></span> <span data-ttu-id="216f3-182">Mesmo no Windows, às vezes é útil obter os dados reais do pixel, e mostramos a maneira atual de fazer isso no exemplo de código abaixo.</span><span class="sxs-lookup"><span data-stu-id="216f3-182">Even on Windows, it's sometimes useful to get the actual pixel data, and we show the current way to do so in the code example below.</span></span>

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a><span data-ttu-id="216f3-183">Outras diferenças de API entre DWriteCore e DirectWrite</span><span class="sxs-lookup"><span data-stu-id="216f3-183">Other API differences between DWriteCore and DirectWrite</span></span>

<span data-ttu-id="216f3-184">Há algumas APIs que são apenas stubs ou que se comportam de maneira um pouco diferente em plataformas que não são do Windows.</span><span class="sxs-lookup"><span data-stu-id="216f3-184">There are a few APIs that are either stubs only, or they behave somewhat differently on non-Windows platforms.</span></span> <span data-ttu-id="216f3-185">Por exemplo, [IDWriteGdiInterop:: CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) retorna **E_NOTIMPL** em plataformas não Windows, já que não há tal coisa como um **HDC** sem [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="216f3-185">For example, [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) returns **E_NOTIMPL** on non-Windows platforms, since there's no such thing as an **HDC** without [GDI](../gdi/windows-gdi.md).</span></span>

<span data-ttu-id="216f3-186">E, finalmente, existem algumas outras APIs do Windows que normalmente são usadas junto com DirectWrite (Direct2D sendo um exemplo notável).</span><span class="sxs-lookup"><span data-stu-id="216f3-186">And, finally, there are certain other Windows APIs that are typically used together with DirectWrite (Direct2D being a notable example).</span></span> <span data-ttu-id="216f3-187">No entanto, atualmente, Direct2D e DWriteCore não interoperam.</span><span class="sxs-lookup"><span data-stu-id="216f3-187">However, currently, Direct2D and DWriteCore don't interoperate.</span></span> <span data-ttu-id="216f3-188">Por exemplo, se você criar um [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) usando DWriteCore e passá-lo para [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), essa chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="216f3-188">For example, if you create an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) using DWriteCore, and pass it to [**D2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), then that call will fail.</span></span>