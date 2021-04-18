---
description: Uma lista de triângulos é uma lista de triângulos isolados. Eles podem ou não estar próximos uns dos outros. Uma lista de triângulos deve ter pelo menos três vértices e o número total de vértices deve ser divisível por três.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listas de triângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791465"
---
# <a name="triangle-lists"></a><span data-ttu-id="32b29-105">Listas de triângulo</span><span class="sxs-lookup"><span data-stu-id="32b29-105">Triangle Lists</span></span>

<span data-ttu-id="32b29-106">Uma lista de triângulos é uma lista de triângulos isolados.</span><span class="sxs-lookup"><span data-stu-id="32b29-106">A triangle list is a list of isolated triangles.</span></span> <span data-ttu-id="32b29-107">Eles podem ou não estar próximos uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="32b29-107">They might or might not be near each other.</span></span> <span data-ttu-id="32b29-108">Uma lista de triângulos deve ter pelo menos três vértices e o número total de vértices deve ser divisível por três.</span><span class="sxs-lookup"><span data-stu-id="32b29-108">A triangle list must have at least three vertices and the total number of vertices must be divisible by three.</span></span>

<span data-ttu-id="32b29-109">Use listas de triângulos para criar um objeto que é composto de peças separadas.</span><span class="sxs-lookup"><span data-stu-id="32b29-109">Use triangle lists to create an object that is composed of disjoint pieces.</span></span> <span data-ttu-id="32b29-110">Por exemplo, uma maneira de criar uma parede de campo de força em um jogo 3D é especificando uma grande lista de triângulos pequenos, desconectados.</span><span class="sxs-lookup"><span data-stu-id="32b29-110">For instance, one way to create a force-field wall in a 3D game is to specify a large list of small, unconnected triangles.</span></span> <span data-ttu-id="32b29-111">Em seguida, aplique um material e textura que parece emitir luz à lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="32b29-111">Then apply a material and texture that appears to emit light to the triangle list.</span></span> <span data-ttu-id="32b29-112">Cada triângulo na parede parece brilhar.</span><span class="sxs-lookup"><span data-stu-id="32b29-112">Each triangle in the wall appears to glow.</span></span> <span data-ttu-id="32b29-113">A cena por trás da parede fica parcialmente visível por meio dos espaços entre os triângulos, da forma que um jogador pode esperar ao olhar para um campo de força.</span><span class="sxs-lookup"><span data-stu-id="32b29-113">The scene behind the wall becomes partially visible through the gaps between the triangles, as a player might expect when looking at a force field.</span></span>

<span data-ttu-id="32b29-114">As listas de triângulo também são úteis para criar primitivos que têm bordas afiadas e são sombreados com sombreamento Gouraud.</span><span class="sxs-lookup"><span data-stu-id="32b29-114">Triangle lists are also useful for creating primitives that have sharp edges and are shaded with Gouraud shading.</span></span> <span data-ttu-id="32b29-115">Consulte [vetores normais de face e vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="32b29-115">See [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

<span data-ttu-id="32b29-116">A ilustração a seguir ilustra uma lista de triângulos renderizada.</span><span class="sxs-lookup"><span data-stu-id="32b29-116">The following illustration depicts a rendered triangle list.</span></span>

![Ilustração de uma lista de triângulos renderizada](images/trilist.png)

<span data-ttu-id="32b29-118">O código a seguir mostra como criar vértices para essa lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="32b29-118">The following code shows how to create vertices for this triangle list.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}

};
```



<span data-ttu-id="32b29-119">O exemplo de código abaixo mostra como renderizar esta lista de triângulos no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="32b29-119">The code example below shows how to render this triangle list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



<span data-ttu-id="32b29-120">Você também pode usar as faixas de triângulo para renderizar triângulos que não estão conectados entre si.</span><span class="sxs-lookup"><span data-stu-id="32b29-120">You can also use triangle strips to render triangles that are not connected to one another.</span></span> <span data-ttu-id="32b29-121">Para fazer isso, especifique um triângulo degenerado (ou seja, um triângulo com tamanho zero) na lista; Isso criará uma linha entre os dois triângulos que não serão exibidos durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="32b29-121">To do this, specify a degenerate triangle (that is, a triangle with zero size) in the list; this will create a line between the two triangles which will not appear during rendering.</span></span> <span data-ttu-id="32b29-122">Por exemplo, para renderizar apenas o primeiro e o último triângulo do exemplo anterior, inicialize o buffer de vértice com os seguintes vértices:</span><span class="sxs-lookup"><span data-stu-id="32b29-122">For example, to render only the first and last triangle from the previous example, initialize the vertex buffer with the following vertices:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="32b29-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32b29-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32b29-124">Primitivos</span><span class="sxs-lookup"><span data-stu-id="32b29-124">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
