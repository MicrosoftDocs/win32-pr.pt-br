---
description: Uma faixa de triângulos é uma série de triângulos conectados.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Faixas de triângulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566234"
---
# <a name="triangle-strips"></a><span data-ttu-id="0af3d-103">Faixas de triângulo</span><span class="sxs-lookup"><span data-stu-id="0af3d-103">Triangle Strips</span></span>

<span data-ttu-id="0af3d-104">Uma faixa de triângulos é uma série de triângulos conectados.</span><span class="sxs-lookup"><span data-stu-id="0af3d-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="0af3d-105">Como os triângulos são conectados, o aplicativo não precisa especificar repetidamente todos os três vértices de cada triângulo.</span><span class="sxs-lookup"><span data-stu-id="0af3d-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="0af3d-106">Por exemplo, você precisa de apenas sete vértices para definir a faixa de triângulos a seguir.</span><span class="sxs-lookup"><span data-stu-id="0af3d-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![ilustração de uma faixa de triângulos com sete vértices](images/tristrip.png)

<span data-ttu-id="0af3d-108">O sistema usa os vértices v1, v2 e v3 para desenhar o primeiro triângulo; v2, v4 e v3 para desenhar o segundo triângulo; v3, v4 e v5 para desenhar o terceiro; V4 e v6 v5 para desenhar o quarto; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0af3d-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="0af3d-109">Observe que os vértices do segundo e do quarto triângulo estão fora de ordem; isso é necessário para garantir que todos os triângulos sejam desenhados em uma orientação no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="0af3d-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="0af3d-110">A maioria dos objetos em cenas 3D são compostos por faixas de triângulos.</span><span class="sxs-lookup"><span data-stu-id="0af3d-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="0af3d-111">Isso ocorre porque as faixas de triângulos podem ser usadas para especificar objetos complexos de maneira a fazer uso eficiente da memória e do tempo de processamento.</span><span class="sxs-lookup"><span data-stu-id="0af3d-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="0af3d-112">A ilustração a seguir ilustra uma faixa de triângulos renderizado.</span><span class="sxs-lookup"><span data-stu-id="0af3d-112">The following illustration depicts a rendered triangle strip.</span></span>

![ilustração de uma faixa de triângulos renderizada](images/tstrip2.png)

<span data-ttu-id="0af3d-114">O código a seguir mostra como criar vértices para essa faixa de triângulos.</span><span class="sxs-lookup"><span data-stu-id="0af3d-114">The following code shows how to create vertices for this triangle strip.</span></span>


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



<span data-ttu-id="0af3d-115">O exemplo de código abaixo mostra como renderizar essa faixa de triângulo no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="0af3d-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="0af3d-116">Use uma faixa de triângulo para renderizar triângulos que não estão conectados entre si.</span><span class="sxs-lookup"><span data-stu-id="0af3d-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="0af3d-117">Para fazer isso, especifique um triângulo degenerado (ou seja, um triângulo cuja área seja zero) na lista de triângulos.</span><span class="sxs-lookup"><span data-stu-id="0af3d-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="0af3d-118">Isso cria uma linha entre os dois triângulos que não serão renderizados.</span><span class="sxs-lookup"><span data-stu-id="0af3d-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="0af3d-119">Para renderizar apenas o primeiro e o último triângulos do exemplo anterior, modifique o buffer de vértice conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="0af3d-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0af3d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0af3d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af3d-121">Primitivos</span><span class="sxs-lookup"><span data-stu-id="0af3d-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
