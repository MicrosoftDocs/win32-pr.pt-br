---
title: Introdução ao DirectX para Windows
description: A criação de um jogo do Microsoft DirectX para Windows é um desafio para um novo desenvolvedor. Aqui, examinamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343581"
---
# <a name="get-started-with-directx-for-windows"></a><span data-ttu-id="97313-104">Introdução ao DirectX para Windows</span><span class="sxs-lookup"><span data-stu-id="97313-104">Get started with DirectX for Windows</span></span>

<span data-ttu-id="97313-105">A criação de um jogo do Microsoft DirectX para Windows é um desafio para um novo desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="97313-105">Creating a Microsoft DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="97313-106">Aqui, examinamos rapidamente os conceitos envolvidos e as etapas que você deve seguir para começar a desenvolver um jogo usando DirectX e C++.</span><span class="sxs-lookup"><span data-stu-id="97313-106">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span>

<span data-ttu-id="97313-107">Vamos começar.</span><span class="sxs-lookup"><span data-stu-id="97313-107">Let's get started.</span></span>

## <a name="what-skills-do-you-need"></a><span data-ttu-id="97313-108">De quais habilidades você precisa?</span><span class="sxs-lookup"><span data-stu-id="97313-108">What skills do you need?</span></span>

<span data-ttu-id="97313-109">Para desenvolver um jogo no DirectX para Windows, você deve ter algumas habilidades básicas.</span><span class="sxs-lookup"><span data-stu-id="97313-109">To develop a game in DirectX for Windows, you must have a few basic skills.</span></span> <span data-ttu-id="97313-110">Especificamente, você deve ser capaz de:</span><span class="sxs-lookup"><span data-stu-id="97313-110">Specifically, you must be able to:</span></span>

-   <span data-ttu-id="97313-111">Leia e escreva código C++ moderno (o C++ 11 ajuda mais) e familiarize-se com os princípios e padrões de design básicos de C++, como modelos e o modelo de fábrica.</span><span class="sxs-lookup"><span data-stu-id="97313-111">Read and write modern C++ code (C++11 helps the most), and be familiar with basic C++ design principles and patterns like templates and the factory model.</span></span> <span data-ttu-id="97313-112">Você também deve estar familiarizado com bibliotecas C++ comuns como a biblioteca de modelos padrão e, especificamente, com os operadores de conversão, tipos de ponteiro e as estruturas de dados da biblioteca de modelos padrão (como std:: vector).</span><span class="sxs-lookup"><span data-stu-id="97313-112">You must also be familiar with common C++ libraries like the Standard Template Library, and specifically with the casting operators, pointer types, and the standard template library data structures (such as std::vector).</span></span>
-   <span data-ttu-id="97313-113">Entenda a geometria básica, a trigonometria e a Algebra linear.</span><span class="sxs-lookup"><span data-stu-id="97313-113">Understand basic geometry, trigonometry, and linear algebra.</span></span> <span data-ttu-id="97313-114">Grande parte do código que você encontrará nos exemplos pressupõe que você compreenda essas formas de matemática e suas regras comuns.</span><span class="sxs-lookup"><span data-stu-id="97313-114">Much of the code you will find in the examples assumes you understand these forms of mathematics and their common rules.</span></span>
-   <span data-ttu-id="97313-115">Familiaridade com com, especialmente [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (ponteiro inteligente).</span><span class="sxs-lookup"><span data-stu-id="97313-115">Have familiarity with COM—especially [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (smart pointer).</span></span>
-   <span data-ttu-id="97313-116">Entenda as bases da tecnologia gráfica e gráfica, especialmente os gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="97313-116">Understand the foundations of graphics and graphics technology, particularly 3D graphics.</span></span> <span data-ttu-id="97313-117">Embora o próprio DirectX tenha sua própria terminologia, ele ainda se baseia em uma compreensão bem estabelecida dos princípios gerais de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="97313-117">While DirectX itself has its own terminology, it still builds upon a well-established understanding of general 3D graphics principles.</span></span>
-   <span data-ttu-id="97313-118">Entenda o conceito de um loop de mensagem, pois você estará implementando um loop que escuta o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="97313-118">Understand the concept of a message loop, because you'll be implementing a loop that listens to the Windows operating system.</span></span>

## <a name="and-were-off"></a><span data-ttu-id="97313-119">E estamos desligados!</span><span class="sxs-lookup"><span data-stu-id="97313-119">And we're off!</span></span>

<span data-ttu-id="97313-120">Pronto para começar?</span><span class="sxs-lookup"><span data-stu-id="97313-120">Ready to start?</span></span> <span data-ttu-id="97313-121">Vamos examinar antes de nosso início.</span><span class="sxs-lookup"><span data-stu-id="97313-121">Let's review before we head on.</span></span> <span data-ttu-id="97313-122">Você:</span><span class="sxs-lookup"><span data-stu-id="97313-122">You have:</span></span>

-   <span data-ttu-id="97313-123">Uma instalação atualizada e funcional do Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="97313-123">An updated and working installation of Windows 8.1.</span></span>
-   <span data-ttu-id="97313-124">Uma instalação do [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span><span class="sxs-lookup"><span data-stu-id="97313-124">An installation of [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).</span></span>
-   <span data-ttu-id="97313-125">Um cérebro intrípido e um desejo de saber mais sobre o desenvolvimento de jogos do DirectX!</span><span class="sxs-lookup"><span data-stu-id="97313-125">An intrepid spirit and a desire to learn more about DirectX game development!</span></span>

## <a name="next-steps"></a><span data-ttu-id="97313-126">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="97313-126">Next steps</span></span>



| <span data-ttu-id="97313-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="97313-127">Topic</span></span>                                                                                                   | <span data-ttu-id="97313-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="97313-128">Description</span></span>                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97313-129">Trabalhar com recursos do dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="97313-129">Work with DirectX device resources</span></span>](work-with-dxgi.md)                                           | <span data-ttu-id="97313-130">Saiba como usar o DXGI para criar um dispositivo gráfico virtualizado e criar e configurar uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="97313-130">Learn how to use DXGI to create a virtualized graphics device, and create and configure a swap chain.</span></span>     |
| [<span data-ttu-id="97313-131">Entender o pipeline de renderização do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="97313-131">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md) | <span data-ttu-id="97313-132">Saiba como conectar-se à classe de recursos do dispositivo DirectX e desenhar usando o pipeline de gráficos direct3D.</span><span class="sxs-lookup"><span data-stu-id="97313-132">Learn how to hook into the DirectX device resources class, and draw using the Direct3D graphics pipeline.</span></span> |
| [<span data-ttu-id="97313-133">Trabalhar com sombreadores e recursos de sombreador</span><span class="sxs-lookup"><span data-stu-id="97313-133">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)               | <span data-ttu-id="97313-134">Saiba como escrever programas de sombreador HLSL para estágios de pipeline de gráficos direct3D.</span><span class="sxs-lookup"><span data-stu-id="97313-134">Learn how to write HLSL shader programs for Direct3D graphics pipeline stages.</span></span>                            |



 

 

 