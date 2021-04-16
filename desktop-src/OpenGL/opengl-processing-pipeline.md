---
title: Pipeline de processamento OpenGL
description: Pipeline de processamento OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline de processamento
- processando o pipeline OpenGL
- pipeline OpenGL
- framebuffers, pipeline de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556328"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="cca2a-107">Pipeline de processamento OpenGL</span><span class="sxs-lookup"><span data-stu-id="cca2a-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="cca2a-108">Muitas funções OpenGL são usadas especificamente para desenhar objetos, como pontos, linhas, polígonos e bitmaps.</span><span class="sxs-lookup"><span data-stu-id="cca2a-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="cca2a-109">Algumas funções controlam a forma como parte desse desenho ocorre (como as que permitem a suavização ou texturing).</span><span class="sxs-lookup"><span data-stu-id="cca2a-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="cca2a-110">Outras funções se preocupam especificamente com a manipulação de framebuffer.</span><span class="sxs-lookup"><span data-stu-id="cca2a-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="cca2a-111">Os tópicos nesta seção descrevem como todas as funções OpenGL funcionam em conjunto para criar o pipeline de processamento OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cca2a-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="cca2a-112">Esta seção também examina mais detalhadamente os estágios em que os dados são realmente processados e vincula esses estágios às funções OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cca2a-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="cca2a-113">O diagrama a seguir detalha o pipeline de processamento do OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cca2a-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="cca2a-114">Para a maior parte do pipeline, você pode ver três setas verticais entre os principais estágios.</span><span class="sxs-lookup"><span data-stu-id="cca2a-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="cca2a-115">Essas setas representam vértices e os dois tipos principais de dados que podem ser associados a vértices: valores de cor e coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="cca2a-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="cca2a-116">Observe também que os vértices são montados em primitivos, em fragmentos e, finalmente, em pixels no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="cca2a-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="cca2a-117">Essa progressão é discutida em mais detalhes em [vértices](vertices.md), [primitivos](primitives.md), [fragmentos](fragments.md)e [pixels](pixels.md).</span><span class="sxs-lookup"><span data-stu-id="cca2a-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![Diagrama mostrando o pipeline de processamento OpenGL.](images/proc01.png)

 

 




