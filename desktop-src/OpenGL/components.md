---
title: Componentes
description: Componentes
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL no Windows, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105782179"
---
# <a name="components"></a><span data-ttu-id="19049-104">Componentes</span><span class="sxs-lookup"><span data-stu-id="19049-104">Components</span></span>

<span data-ttu-id="19049-105">A implementação da Microsoft do OpenGL no Windows inclui os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="19049-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="19049-106">O conjunto completo de comandos OpenGL atuais</span><span class="sxs-lookup"><span data-stu-id="19049-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="19049-107">O OpenGL contém uma biblioteca de funções básicas para operações de gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="19049-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="19049-108">Essas funções básicas são usadas para gerenciar a descrição da forma de objeto, transformação de matriz, iluminação, coloração, textura, recorte, bitmaps, neblina e anti-aliasing.</span><span class="sxs-lookup"><span data-stu-id="19049-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="19049-109">Os nomes dessas funções principais têm um prefixo "GL".</span><span class="sxs-lookup"><span data-stu-id="19049-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="19049-110">Muitos dos comandos OpenGL têm várias variantes, que diferem no número e no tipo de seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="19049-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="19049-111">Contando todas as variantes, há mais de 300 comandos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="19049-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="19049-112">A biblioteca do utilitário OpenGL (GLU)</span><span class="sxs-lookup"><span data-stu-id="19049-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="19049-113">Essa biblioteca de funções auxiliares complementa as principais funções OpenGL.</span><span class="sxs-lookup"><span data-stu-id="19049-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="19049-114">Os comandos gerenciam o suporte à textura, a transformação de coordenadas, o mosaico de polígono, a renderização de difira, cilindros e discos, curvas e superfícies de NURBS (não uniforme, B-spline) e tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="19049-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="19049-115">A biblioteca auxiliar do guia de programação OpenGL</span><span class="sxs-lookup"><span data-stu-id="19049-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="19049-116">Essa é uma biblioteca de funções simples e independente de plataforma para gerenciar o Windows, manipular eventos de entrada, desenhar objetos 3D clássicos, gerenciar um processo em segundo plano e executar um programa.</span><span class="sxs-lookup"><span data-stu-id="19049-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="19049-117">O gerenciamento de janelas e as rotinas de entrada fornecem um nível básico de funcionalidade com o qual você pode começar a programação rapidamente no OpenGL.</span><span class="sxs-lookup"><span data-stu-id="19049-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="19049-118">Não os use, no entanto, em um aplicativo de produção.</span><span class="sxs-lookup"><span data-stu-id="19049-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="19049-119">Aqui estão alguns motivos para esse aviso:</span><span class="sxs-lookup"><span data-stu-id="19049-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="19049-120">O loop de mensagem está no código de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="19049-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="19049-121">Não há nenhuma maneira de adicionar manipuladores para mensagens adicionais do WM \* .</span><span class="sxs-lookup"><span data-stu-id="19049-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="19049-122">Há muito pouco suporte para paletas lógicas.</span><span class="sxs-lookup"><span data-stu-id="19049-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="19049-123">A biblioteca é descrita e usada no *Guia de programação OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="19049-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="19049-124">As funções WGL</span><span class="sxs-lookup"><span data-stu-id="19049-124">The WGL functions</span></span>

    <span data-ttu-id="19049-125">Esse conjunto de funções conecta o OpenGL ao sistema de janelas do Windows.</span><span class="sxs-lookup"><span data-stu-id="19049-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="19049-126">As funções gerenciam contextos de renderização, listas de exibição, funções de extensão e bitmaps de fontes.</span><span class="sxs-lookup"><span data-stu-id="19049-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="19049-127">As funções WGL são análogas às extensões GLX que conectam OpenGL ao sistema de janelas X.</span><span class="sxs-lookup"><span data-stu-id="19049-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="19049-128">Os nomes dessas funções têm um prefixo "WGL".</span><span class="sxs-lookup"><span data-stu-id="19049-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="19049-129">Novas funções do Windows para formatos de pixel e buffer duplo</span><span class="sxs-lookup"><span data-stu-id="19049-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="19049-130">Essas funções dão suporte a formatos de pixel por janela e buffer duplo (para alterações de imagem suave) do Windows.</span><span class="sxs-lookup"><span data-stu-id="19049-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="19049-131">Essas novas funções se aplicam somente a janelas de gráficos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="19049-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




