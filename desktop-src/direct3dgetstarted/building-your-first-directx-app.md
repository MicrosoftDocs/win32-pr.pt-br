---
title: Crie seu primeiro aplicativo do Windows usando DirectX
description: Esta seção descreve por que você usaria o modelo C++ para desenvolvimento de aplicativos da Windows Store e fornece tutoriais e procedimentos básicos para a introdução ao desenvolvimento de aplicativos DirectX.
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- Aplicativo DirectX, guia de introdução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634786"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="8b70d-104">Crie seu primeiro aplicativo do Windows usando DirectX</span><span class="sxs-lookup"><span data-stu-id="8b70d-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="8b70d-105">Se você conhece o DirectX, pode desenvolver um aplicativo DirectX usando C++ nativo e HLSL para aproveitar ao máximo o hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="8b70d-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="8b70d-106">Use este tutorial básico para começar a usar o desenvolvimento de aplicativos DirectX e, em seguida, use o roteiro para continuar explorando o DirectX.</span><span class="sxs-lookup"><span data-stu-id="8b70d-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="8b70d-107">Aplicativo de área de trabalho do Windows com C++ e DirectX</span><span class="sxs-lookup"><span data-stu-id="8b70d-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="8b70d-108">Um aplicativo de área de trabalho do Windows com DirectX é um aplicativo desenvolvido usando APIs nativas do C++ e do DirectX.</span><span class="sxs-lookup"><span data-stu-id="8b70d-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="8b70d-109">Esse modelo é mais complexo do que um aplicativo escrito em uma estrutura gerenciada, mas fornece maior flexibilidade e mais acesso a recursos do sistema especialmente dispositivos gráficos.</span><span class="sxs-lookup"><span data-stu-id="8b70d-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="8b70d-110">Portanto, é um bom modelo para o desenvolvedor experiente.</span><span class="sxs-lookup"><span data-stu-id="8b70d-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="8b70d-111">Por que desenvolver um aplicativo do Windows com o DirectX?</span><span class="sxs-lookup"><span data-stu-id="8b70d-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="8b70d-112">A resposta é simples: você deseja criar um jogo com uso intensivo de gráficos ou de multimídia e pode usar os recursos que muitos dispositivos gráficos dão suporte.</span><span class="sxs-lookup"><span data-stu-id="8b70d-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="8b70d-113">Isso não será fácil se você for novo no desenvolvimento de jogos ou no desenvolvimento para Windows e C/C++, mas houver algumas boas notícias: o DirectX 11 é a versão mais simples e coesa do Microsoft DirectX ainda.</span><span class="sxs-lookup"><span data-stu-id="8b70d-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="8b70d-114">Ele também é o mais potente e repleto de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b70d-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="8b70d-115">Se seu objetivo é fazer o desenvolvimento mestre de jogos e aprender as técnicas de renderização mais avançadas, o DirectX pode fornecer a oportunidade para você fazer isso.</span><span class="sxs-lookup"><span data-stu-id="8b70d-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="8b70d-116">Dito isso, planejar seu jogo (ou aplicativo interativo em tempo real) é essencial.</span><span class="sxs-lookup"><span data-stu-id="8b70d-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="8b70d-117">Se você for novo no desenvolvimento de jogos e seu jogo não tiver requisitos gráficos exigentes, considere o desenvolvimento dele com o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8b70d-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="8b70d-118">Além disso, muitos gráficos de "middleware" e pacotes de desenvolvimento de jogos estão disponíveis para plataformas Windows e alguns não exigem habilidades significativas de programação.</span><span class="sxs-lookup"><span data-stu-id="8b70d-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="8b70d-119">Se você estiver confiante ou simplesmente tiver um sonho em fazer um jogo com gráficos de alta fidelidade (ou um aplicativo com conteúdo de gráficos complexo), continue lendo!</span><span class="sxs-lookup"><span data-stu-id="8b70d-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8b70d-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8b70d-120">In this section</span></span>



| <span data-ttu-id="8b70d-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="8b70d-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="8b70d-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b70d-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b70d-123">Pré-requisitos para o desenvolvimento com DirectX</span><span class="sxs-lookup"><span data-stu-id="8b70d-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="8b70d-124">Ao começar a desenvolver um aplicativo do Windows usando o DirectX, mantenha os pré-requisitos nessa página em mente.</span><span class="sxs-lookup"><span data-stu-id="8b70d-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="8b70d-125">Isso inclui as tecnologias que você precisa saber antes de se aprofundar.</span><span class="sxs-lookup"><span data-stu-id="8b70d-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="8b70d-126">Introdução ao DirectX para Windows</span><span class="sxs-lookup"><span data-stu-id="8b70d-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="8b70d-127">Criar um jogo DirectX para o Windows é um desafio para um novo desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="8b70d-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="8b70d-128">Aqui, examinamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.</span><span class="sxs-lookup"><span data-stu-id="8b70d-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="8b70d-129">Roteiro para aplicativos DirectX para Desktop</span><span class="sxs-lookup"><span data-stu-id="8b70d-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="8b70d-130">Aqui estão os principais recursos para ajudá-lo a começar a usar o DirectX e o C++ para desenvolver aplicativos de área de trabalho com uso intensivo de gráficos, como jogos.</span><span class="sxs-lookup"><span data-stu-id="8b70d-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





