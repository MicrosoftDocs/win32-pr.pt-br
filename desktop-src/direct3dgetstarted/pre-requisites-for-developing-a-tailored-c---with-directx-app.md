---
title: Pré-requisitos para o desenvolvimento com DirectX
description: Ao começar a desenvolver um aplicativo do Windows usando o DirectX, mantenha os pré-requisitos nessa página em mente. Isso inclui as tecnologias que você precisa saber antes de se aprofundar.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Aplicativo DirectX, pré-requisitos
- Aplicativo DirectX, aplicativo da Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/16/2020
ms.locfileid: "104454480"
---
# <a name="prerequisites-for-developing-with-directx"></a><span data-ttu-id="58173-106">Pré-requisitos para o desenvolvimento com DirectX</span><span class="sxs-lookup"><span data-stu-id="58173-106">Prerequisites for developing with DirectX</span></span>

<span data-ttu-id="58173-107">Ao começar a desenvolver um aplicativo do Windows usando o DirectX, mantenha os pré-requisitos nessa página em mente.</span><span class="sxs-lookup"><span data-stu-id="58173-107">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="58173-108">Isso inclui as tecnologias que você precisa saber antes de se aprofundar.</span><span class="sxs-lookup"><span data-stu-id="58173-108">This includes the technologies you need to know before you dive in.</span></span>

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a><span data-ttu-id="58173-109">O que devo saber para desenvolver um jogo do Windows usando o DirectX?</span><span class="sxs-lookup"><span data-stu-id="58173-109">What should I know to develop a Windows game using DirectX?</span></span>

<span data-ttu-id="58173-110">Antes de começar a desenvolver um aplicativo da Windows Store usando o DirectX, você precisa saber como programar no Windows com o C++.</span><span class="sxs-lookup"><span data-stu-id="58173-110">Before you start to develop a Windows Store app using DirectX, you need to know how to program in Windows with C++.</span></span> <span data-ttu-id="58173-111">Os aplicativos do Windows que usam o DirectX são desenvolvidos em um nível baixo de programação, o que significa que você será exposto a muitos recursos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="58173-111">Windows apps using DirectX are developed at a low level of programming, which means that you will be exposed to many features of the operating system.</span></span> <span data-ttu-id="58173-112">Isso inclui memória e gerenciamento de recursos e a interface para o próprio dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="58173-112">These include memory and resource management, and the interface for the graphics device itself.</span></span> <span data-ttu-id="58173-113">Se você for novo no desenvolvimento de aplicativos gráficos ou de jogos, poderá achar esse desafio.</span><span class="sxs-lookup"><span data-stu-id="58173-113">If you are new to game or graphics app development, you may find this challenging.</span></span> <span data-ttu-id="58173-114">Mas você também encontrará a gratificação de ti, pois o aprendizado do desenvolvimento de jogos nesse nível cria possibilidades muito mais distantes para design e desenvolvimento de aplicativos gráficos e jogos.</span><span class="sxs-lookup"><span data-stu-id="58173-114">But you will also find it rewarding, because learning game development at this level creates far, far greater possibilities for game and graphics app design and development.</span></span>

<span data-ttu-id="58173-115">Você também precisará compreender as noções básicas de programação de gráficos 2D e 3D e matemática, pois muitas das APIs que você usaram foram desenvolvidas com esses princípios em mente.</span><span class="sxs-lookup"><span data-stu-id="58173-115">You'll also need to understand the basics of 2D and 3D graphics programming and mathematics, because many of the APIs you'll use were developed with these principles in mind.</span></span> <span data-ttu-id="58173-116">Será mais fácil entender seus parâmetros e resultados se você estiver familiarizado com as operações por trás deles.</span><span class="sxs-lookup"><span data-stu-id="58173-116">It'll be easier for you to understand their parameters and results if you are familiar with the operations behind them.</span></span>

<span data-ttu-id="58173-117">No mínimo, você deve ter uma noção do seguinte:</span><span class="sxs-lookup"><span data-stu-id="58173-117">At a minimum, you should have a grasp of the following:</span></span>

-   <span data-ttu-id="58173-118">Programação C/C++ do Windows.</span><span class="sxs-lookup"><span data-stu-id="58173-118">Windows C/C++ programming.</span></span> <span data-ttu-id="58173-119">Isso significa que você entende ponteiros e referências, eventos e retornos de chamada, e talvez algumas das bibliotecas comuns, como a ATL.</span><span class="sxs-lookup"><span data-stu-id="58173-119">This means that you understand pointers and references, events and callbacks, and perhaps a few of the common libraries like ATL.</span></span>
-   <span data-ttu-id="58173-120">Programação do Win32.</span><span class="sxs-lookup"><span data-stu-id="58173-120">Win32 programming.</span></span> <span data-ttu-id="58173-121">Você entende como o Windows é criado e como os eventos da interface do usuário são processados.</span><span class="sxs-lookup"><span data-stu-id="58173-121">You understand how windows are created, and how user interface events are processed.</span></span> <span data-ttu-id="58173-122">Você também entende um pouco sobre o COM e as APIs do Win32 essenciais.</span><span class="sxs-lookup"><span data-stu-id="58173-122">You also understand a little bit about COM and essential Win32 APIs.</span></span>
-   <span data-ttu-id="58173-123">Algebra linear e trigonometria.</span><span class="sxs-lookup"><span data-stu-id="58173-123">Linear algebra and trigonometry.</span></span> <span data-ttu-id="58173-124">Embora não seja essencial, você terá um tempo mais fácil se estiver familiarizado com os conceitos dessas duas disciplinas matemáticas, pois elas são a base de grande parte da programação de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="58173-124">While not essential, you'll have an easier time if you are familiar with concepts from these two math disciplines, because they are the foundation of much of 3D graphics programming.</span></span>
-   <span data-ttu-id="58173-125">Terminologia e conceitos básicos de gráficos, como bitmaps, texturas, vértices, malhas e visores.</span><span class="sxs-lookup"><span data-stu-id="58173-125">Basic graphics terminology and concepts, such as bitmaps, textures, vertices, meshes, and viewports.</span></span>

## <a name="what-does-directx-provide-me"></a><span data-ttu-id="58173-126">O que o DirectX fornece?</span><span class="sxs-lookup"><span data-stu-id="58173-126">What does DirectX provide me?</span></span>

<span data-ttu-id="58173-127">O DirectX é o principal conjunto de APIs de gráficos que você usará para desenvolver jogos do Windows.</span><span class="sxs-lookup"><span data-stu-id="58173-127">DirectX is the primary set of graphics APIs you'll use to develop Windows games.</span></span> <span data-ttu-id="58173-128">Aqui estão as categorias de recursos com os quais você deve se familiarizar quando decidir como desenvolver seu jogo.</span><span class="sxs-lookup"><span data-stu-id="58173-128">Here are the categories of features that you must become familiar with when you decide how to develop your game.</span></span>



| <span data-ttu-id="58173-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58173-129">Library</span></span>     | <span data-ttu-id="58173-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="58173-130">Description</span></span>                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58173-131">Direct3D</span><span class="sxs-lookup"><span data-stu-id="58173-131">Direct3D</span></span>    | <span data-ttu-id="58173-132">Um conjunto avançado, orientado por desempenho e acelerado por hardware de bibliotecas para renderizar gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="58173-132">A powerful, performance-oriented, hardware-accelerated set of libraries for rendering 3D graphics.</span></span>                                              |
| <span data-ttu-id="58173-133">Direct2D</span><span class="sxs-lookup"><span data-stu-id="58173-133">Direct2D</span></span>    | <span data-ttu-id="58173-134">Um conjunto de bibliotecas gráficas 2D para bitmap com aceleração de hardware e desenho 2D de vetor.</span><span class="sxs-lookup"><span data-stu-id="58173-134">A set of 2D graphics libraries for hardware-accelerated bitmap and vector 2D drawing.</span></span>                                                           |
| <span data-ttu-id="58173-135">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="58173-135">DirectXMath</span></span> | <span data-ttu-id="58173-136">Uma biblioteca de operações matemáticas comuns e otimizadas usadas em gráficos 2D e 3D, como operações de vetor e matriz.</span><span class="sxs-lookup"><span data-stu-id="58173-136">A library of common, optimized math operations used in 2D and 3D graphics, such as vector and matrix operations.</span></span>                                |
| <span data-ttu-id="58173-137">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="58173-137">DirectWrite</span></span> | <span data-ttu-id="58173-138">Uma biblioteca de APIs de renderização e layout de texto 2D.</span><span class="sxs-lookup"><span data-stu-id="58173-138">A library of 2D text rendering and layout APIs.</span></span> <span data-ttu-id="58173-139">Ele dá suporte à aceleração de hardware e à rasterização de software.</span><span class="sxs-lookup"><span data-stu-id="58173-139">It supports both hardware acceleration and software rasterization.</span></span>                              |
| <span data-ttu-id="58173-140">XAudio2</span><span class="sxs-lookup"><span data-stu-id="58173-140">XAudio2</span></span>     | <span data-ttu-id="58173-141">Uma API de áudio de plataforma cruzada de baixo nível para o Microsoft Windows que fornece processamento de sinal e base de mixagem de áudio para desenvolvimento de jogos.</span><span class="sxs-lookup"><span data-stu-id="58173-141">A low-level, cross-platform audio API for Microsoft Windows that provides a signal processing and audio mixing foundation for game development.</span></span> |
| <span data-ttu-id="58173-142">XInput</span><span class="sxs-lookup"><span data-stu-id="58173-142">XInput</span></span>      | <span data-ttu-id="58173-143">Uma biblioteca que dá suporte a vários controles de jogos tradicionais, com ênfase no modelo de controlador do Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="58173-143">A library that supports various traditional gaming controls, with an emphasis on the Xbox 360 controller model.</span></span>                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a><span data-ttu-id="58173-144">Quais ferramentas preciso para desenvolver um jogo do Windows com o DirectX?</span><span class="sxs-lookup"><span data-stu-id="58173-144">What tools do I need to develop a Windows game with DirectX?</span></span>

<span data-ttu-id="58173-145">Para começar a usar este tutorial, você precisará de:</span><span class="sxs-lookup"><span data-stu-id="58173-145">To get started with this tutorial, you need:</span></span>

-   <span data-ttu-id="58173-146">Windows 8.1 ou superior</span><span class="sxs-lookup"><span data-stu-id="58173-146">Windows 8.1 or greater</span></span>
-   <span data-ttu-id="58173-147">Microsoft Visual Studio 2013 ou superior</span><span class="sxs-lookup"><span data-stu-id="58173-147">Microsoft Visual Studio 2013 or greater</span></span>

 

 




