---
description: 'Os serviços do Windows GDI+ se enquadram nas três categorias amplas a seguir:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: As três partes do GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988858"
---
# <a name="the-three-parts-of-gdi"></a><span data-ttu-id="043ce-103">As três partes do GDI+</span><span class="sxs-lookup"><span data-stu-id="043ce-103">The Three Parts of GDI+</span></span>

<span data-ttu-id="043ce-104">Os serviços do Windows GDI+ se enquadram nas três categorias amplas a seguir:</span><span class="sxs-lookup"><span data-stu-id="043ce-104">The services of Windows GDI+ fall into the following three broad categories:</span></span>

-   [<span data-ttu-id="043ce-105">gráficos vetoriais 2D</span><span class="sxs-lookup"><span data-stu-id="043ce-105">2-D vector graphics</span></span>](#2-d-vector-graphics)
-   [<span data-ttu-id="043ce-106">Geração de imagens</span><span class="sxs-lookup"><span data-stu-id="043ce-106">Imaging</span></span>](#imaging)
-   [<span data-ttu-id="043ce-107">Tipografia</span><span class="sxs-lookup"><span data-stu-id="043ce-107">Typography</span></span>](#typography)

## <a name="2-d-vector-graphics"></a><span data-ttu-id="043ce-108">gráfico vetorial 2D</span><span class="sxs-lookup"><span data-stu-id="043ce-108">2-D vector graphics</span></span>

<span data-ttu-id="043ce-109">Os gráficos vetoriais envolvem primitivas de desenho (como linhas, curvas e figuras) que são especificadas por conjuntos de pontos em um sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="043ce-109">Vector graphics involves drawing primitives (such as lines, curves, and figures) that are specified by sets of points on a coordinate system.</span></span> <span data-ttu-id="043ce-110">Por exemplo, uma linha reta pode ser especificada por seus dois pontos de extremidade, e um retângulo pode ser especificado por um ponto dando o local de seu canto superior esquerdo e um par de números que dão sua largura e altura.</span><span class="sxs-lookup"><span data-stu-id="043ce-110">For example, a straight line can be specified by its two endpoints, and a rectangle can be specified by a point giving the location of its upper-left corner and a pair of numbers giving its width and height.</span></span> <span data-ttu-id="043ce-111">Um caminho simples pode ser especificado por uma matriz de pontos a ser conectada por linhas retas.</span><span class="sxs-lookup"><span data-stu-id="043ce-111">A simple path can be specified by an array of points to be connected by straight lines.</span></span> <span data-ttu-id="043ce-112">Uma spline de Bézier é uma curva sofisticada especificada por quatro pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="043ce-112">A Bézier spline is a sophisticated curve specified by four control points.</span></span>

<span data-ttu-id="043ce-113">O GDI+ fornece classes que armazenam informações sobre os próprios primitivos, classes que armazenam informações sobre como os primitivos devem ser desenhados e classes que realmente fazem o desenho.</span><span class="sxs-lookup"><span data-stu-id="043ce-113">GDI+ provides classes that store information about the primitives themselves, classes that store information about how the primitives are to be drawn, and classes that actually do the drawing.</span></span> <span data-ttu-id="043ce-114">Por exemplo, a classe **Rect** armazena o local e o tamanho de um retângulo; a classe Pen armazena informações sobre a cor da linha, a largura da linha e o estilo **da** linha; e a classe **Graphics** tem métodos para desenhar linhas, retângulos, caminhos e outras figuras.</span><span class="sxs-lookup"><span data-stu-id="043ce-114">For example, the **Rect** class stores the location and size of a rectangle; the **Pen** class stores information about line color, line width, and line style; and the **Graphics** class has methods for drawing lines, rectangles, paths, and other figures.</span></span> <span data-ttu-id="043ce-115">Há também várias classes de **pincel** que armazenam informações sobre como figuras e caminhos fechados devem ser preenchidos com cores ou padrões.</span><span class="sxs-lookup"><span data-stu-id="043ce-115">There are also several **Brush** classes that store information about how closed figures and paths are to be filled with colors or patterns.</span></span>

## <a name="imaging"></a><span data-ttu-id="043ce-116">Geração de imagens</span><span class="sxs-lookup"><span data-stu-id="043ce-116">Imaging</span></span>

<span data-ttu-id="043ce-117">Determinados tipos de imagens são difíceis ou impossíveis de exibir com as técnicas de gráficos vetoriais.</span><span class="sxs-lookup"><span data-stu-id="043ce-117">Certain kinds of pictures are difficult or impossible to display with the techniques of vector graphics.</span></span> <span data-ttu-id="043ce-118">Por exemplo, as imagens nos botões da barra de ferramentas e as imagens que aparecem como ícones seriam difíceis de especificar como coleções de linhas e curvas.</span><span class="sxs-lookup"><span data-stu-id="043ce-118">For example, the pictures on toolbar buttons and the pictures that appear as icons would be difficult to specify as collections of lines and curves.</span></span> <span data-ttu-id="043ce-119">Uma fotografia digital de alta resolução de um estádio de beisebol lotado seria ainda mais difícil de criar com técnicas vetoriais.</span><span class="sxs-lookup"><span data-stu-id="043ce-119">A high-resolution digital photograph of a crowded baseball stadium would be even more difficult to create with vector techniques.</span></span> <span data-ttu-id="043ce-120">As imagens desse tipo são armazenadas como bitmaps, matrizes de números que representam as cores de pontos individuais na tela.</span><span class="sxs-lookup"><span data-stu-id="043ce-120">Images of this type are stored as bitmaps, arrays of numbers that represent the colors of individual dots on the screen.</span></span> <span data-ttu-id="043ce-121">As estruturas de dados que armazenam informações sobre bitmaps tendem a ser mais complexas do que aquelas necessárias para gráficos vetoriais, portanto, há várias classes em GDI+ dedicadas a essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="043ce-121">Data structures that store information about bitmaps tend to be more complex than those required for vector graphics, so there are several classes in GDI+ devoted to this purpose.</span></span> <span data-ttu-id="043ce-122">Um exemplo de tal classe é **CachedBitmap**, que é usado para armazenar um bitmap na memória para acesso rápido e exibição.</span><span class="sxs-lookup"><span data-stu-id="043ce-122">An example of such a class is **CachedBitmap**, which is used to store a bitmap in memory for fast access and display.</span></span>

## <a name="typography"></a><span data-ttu-id="043ce-123">Tipografia</span><span class="sxs-lookup"><span data-stu-id="043ce-123">Typography</span></span>

<span data-ttu-id="043ce-124">A tipografia se preocupa com a exibição de texto em uma variedade de fontes, tamanhos e estilos.</span><span class="sxs-lookup"><span data-stu-id="043ce-124">Typography is concerned with the display of text in a variety of fonts, sizes, and styles.</span></span> <span data-ttu-id="043ce-125">O GDI+ fornece uma grande quantidade de suporte para essa tarefa complexa.</span><span class="sxs-lookup"><span data-stu-id="043ce-125">GDI+ provides an impressive amount of support for this complex task.</span></span> <span data-ttu-id="043ce-126">Um dos novos recursos do GDI+ é a suavização de subpixel, o que dá ao texto renderizado em uma tela de LCD uma aparência mais suave.</span><span class="sxs-lookup"><span data-stu-id="043ce-126">One of the new features in GDI+ is subpixel antialiasing, which gives text rendered on an LCD screen a smoother appearance.</span></span>

 

 



