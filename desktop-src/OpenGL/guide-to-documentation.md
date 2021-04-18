---
title: Guia de documentação
description: A documentação definida para OpenGL no Windows inclui cinco elementos.
ms.assetid: 1672e9a3-10f0-4ae4-a6a3-b482a3bdda10
keywords:
- OpenGL no Windows, documentação
- Manual de referência OpenGL
- Guia de programação OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc27d11b8d829efebf0914dbb1d67c872cf0196d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756884"
---
# <a name="guide-to-documentation"></a><span data-ttu-id="e4f17-106">Guia de documentação</span><span class="sxs-lookup"><span data-stu-id="e4f17-106">Guide To Documentation</span></span>

<span data-ttu-id="e4f17-107">A documentação definida para OpenGL no Windows inclui cinco elementos.</span><span class="sxs-lookup"><span data-stu-id="e4f17-107">The documentation set for OpenGL in Windows includes five elements.</span></span>

-   <span data-ttu-id="e4f17-108">O *manual de referência do OpenGL* inclui uma visão geral de como o OpenGL funciona e um conjunto de páginas de referência detalhadas.</span><span class="sxs-lookup"><span data-stu-id="e4f17-108">The *OpenGL Reference Manual* includes an overview of how OpenGL works and a set of detailed reference pages.</span></span> <span data-ttu-id="e4f17-109">As páginas de referência abrangem todas as 115 funções OpenGL distintas, bem como as funções 43 na biblioteca do utilitário OpenGL (GLU).</span><span class="sxs-lookup"><span data-stu-id="e4f17-109">The reference pages cover all the 115 distinct OpenGL functions, as well as the 43 functions in the OpenGL Utility (GLU) library.</span></span>

-   <span data-ttu-id="e4f17-110">O *Guia de programação OpenGL* explica como criar programas gráficos usando OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e4f17-110">The *OpenGL Programming Guide* explains how to create graphics programs using OpenGL.</span></span> <span data-ttu-id="e4f17-111">Ele inclui discussões dos seguintes tópicos principais:</span><span class="sxs-lookup"><span data-stu-id="e4f17-111">It includes discussions of the following major topics:</span></span>

    -   <span data-ttu-id="e4f17-112">Desenho de formas geométricas</span><span class="sxs-lookup"><span data-stu-id="e4f17-112">Drawing geometric shapes</span></span>
    -   <span data-ttu-id="e4f17-113">Pixels, bitmaps, fontes e imagens</span><span class="sxs-lookup"><span data-stu-id="e4f17-113">Pixels, bitmaps, fonts, and images</span></span>
    -   <span data-ttu-id="e4f17-114">Exibindo e transformações de matriz</span><span class="sxs-lookup"><span data-stu-id="e4f17-114">Viewing and matrix transformations</span></span>
    -   <span data-ttu-id="e4f17-115">Mapeamento de textura</span><span class="sxs-lookup"><span data-stu-id="e4f17-115">Texture mapping</span></span>
    -   <span data-ttu-id="e4f17-116">Exibir listas</span><span class="sxs-lookup"><span data-stu-id="e4f17-116">Display lists</span></span>
    -   <span data-ttu-id="e4f17-117">Técnicas compostas avançadas</span><span class="sxs-lookup"><span data-stu-id="e4f17-117">Advanced composite techniques</span></span>
    -   <span data-ttu-id="e4f17-118">Cor</span><span class="sxs-lookup"><span data-stu-id="e4f17-118">Color</span></span>
    -   <span data-ttu-id="e4f17-119">Avaliadores e NURBS</span><span class="sxs-lookup"><span data-stu-id="e4f17-119">Evaluators and NURBS</span></span>
    -   <span data-ttu-id="e4f17-120">Iluminação</span><span class="sxs-lookup"><span data-stu-id="e4f17-120">Lighting</span></span>
    -   <span data-ttu-id="e4f17-121">Seleção e comentários</span><span class="sxs-lookup"><span data-stu-id="e4f17-121">Selection and feedback</span></span>
    -   <span data-ttu-id="e4f17-122">Mesclagem, suavização e neblina</span><span class="sxs-lookup"><span data-stu-id="e4f17-122">Blending, antialiasing, and fog</span></span>
    -   <span data-ttu-id="e4f17-123">Técnicas avançadas</span><span class="sxs-lookup"><span data-stu-id="e4f17-123">Advanced techniques</span></span>

    <span data-ttu-id="e4f17-124">Além disso, o *Guia de programação OpenGL* contém apêndices que abordam a biblioteca do utilitário OpenGL e a biblioteca auxiliar do guia de programação OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e4f17-124">In addition, the *OpenGL Programming Guide* contains appendixes that discuss the OpenGL Utility library and the OpenGL Programming Guide Auxiliary library.</span></span>

-   <span data-ttu-id="e4f17-125">O terceiro elemento de documentação é esta visão geral.</span><span class="sxs-lookup"><span data-stu-id="e4f17-125">The third documentation element is this overview.</span></span> <span data-ttu-id="e4f17-126">Ele descreve a implementação do OpenGL do Windows e fornece uma visão geral de seus componentes.</span><span class="sxs-lookup"><span data-stu-id="e4f17-126">It describes the Windows implementation of OpenGL and provides an overview of its components.</span></span> <span data-ttu-id="e4f17-127">Ele aborda os conceitos de contextos de renderização, formatos de pixel e buffers; as funções WGL que conectam OpenGL aos sistemas de janelas do Windows; e as funções do Windows que dão suporte a formatos de pixel por janela e buffer duplo do Windows para janelas de gráficos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e4f17-127">It discusses the concepts of rendering contexts, pixel formats, and buffers; the WGL functions that connect OpenGL to the Windows windowing systems; and the Windows functions that support per-window pixel formats and double buffering of windows for OpenGL graphics windows.</span></span> <span data-ttu-id="e4f17-128">As funções WGL e as funções são específicas para a implementação do OpenGL do Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f17-128">The WGL functions and the functions are specific to the Windows implementation of OpenGL.</span></span>

-   <span data-ttu-id="e4f17-129">O quarto elemento de documentação é o conjunto de páginas de referência para as funções WGL, as funções do Windows que acabamos de mencionar e a estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="e4f17-129">The fourth documentation element is the set of reference pages for the WGL functions, the Windows functions just mentioned, and the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span>

-   <span data-ttu-id="e4f17-130">O quinto elemento de documentação é o guia de portabilidade.</span><span class="sxs-lookup"><span data-stu-id="e4f17-130">The fifth documentation element is the porting guide.</span></span> <span data-ttu-id="e4f17-131">Ele aborda a movimentação do código OpenGL existente de outros ambientes para o Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f17-131">It discusses moving existing OpenGL code from other environments to Windows.</span></span>

<span data-ttu-id="e4f17-132">Os dois primeiros elementos são os manuais OpenGL oficiais; Eles não são incluídos no SDK do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f17-132">The first two elements are the official OpenGL books; they are not included in the Microsoft Windows SDK.</span></span>

 

 




