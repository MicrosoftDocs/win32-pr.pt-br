---
description: O modo de sombreamento usado para renderizar um polígono tem um efeito profundo sobre sua aparência. Os modos de sombreamento determinam a intensidade de cor e iluminação em qualquer ponto em um título de polígono. O Direct3D dá suporte a dois modos de sombreamento.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modos de sombreamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558223"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="b8035-105">Modos de sombreamento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b8035-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="b8035-106">O modo de sombreamento usado para renderizar um polígono tem um efeito profundo sobre sua aparência.</span><span class="sxs-lookup"><span data-stu-id="b8035-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="b8035-107">Os modos de sombreamento determinam a intensidade de cor e iluminação em qualquer ponto em um título de polígono.</span><span class="sxs-lookup"><span data-stu-id="b8035-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="b8035-108">O Direct3D dá suporte a dois modos de sombreamento.</span><span class="sxs-lookup"><span data-stu-id="b8035-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="b8035-109">Sombreamento simples</span><span class="sxs-lookup"><span data-stu-id="b8035-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="b8035-110">Sombreamento Gouraud</span><span class="sxs-lookup"><span data-stu-id="b8035-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="b8035-111">Sombreamento simples</span><span class="sxs-lookup"><span data-stu-id="b8035-111">Flat Shading</span></span>

<span data-ttu-id="b8035-112">No modo de sombreamento simples, o pipeline de renderização do Direct3D renderiza um polígono, usando a cor do material do polígono em seu primeiro vértice como a cor do polígono inteiro.</span><span class="sxs-lookup"><span data-stu-id="b8035-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="b8035-113">objetos 3D que são renderizados com sombreamento simples têm bordas nítidas visivelmente entre polígonos se não forem coplanar.</span><span class="sxs-lookup"><span data-stu-id="b8035-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="b8035-114">A ilustração a seguir mostra um bule renderizado com sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="b8035-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="b8035-115">O contorno de cada polígono é claramente visível.</span><span class="sxs-lookup"><span data-stu-id="b8035-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="b8035-116">O sombreamento simples é a forma mais rápida de sombreamento.</span><span class="sxs-lookup"><span data-stu-id="b8035-116">Flat shading is the fastest form of shading.</span></span>

![ilustração de um bule usando sombreamento simples](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="b8035-118">Sombreamento Gouraud</span><span class="sxs-lookup"><span data-stu-id="b8035-118">Gouraud Shading</span></span>

<span data-ttu-id="b8035-119">Quando o Direct3D renderiza um polígono usando sombreamento Gouraud, ele computa uma cor para cada vértice usando os parâmetros normal de vértice e iluminação.</span><span class="sxs-lookup"><span data-stu-id="b8035-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="b8035-120">Em seguida, ele interpola a cor na face dos polígonos que a interpolação é feita linearmente.</span><span class="sxs-lookup"><span data-stu-id="b8035-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="b8035-121">Por exemplo, se o componente vermelho da cor do vértice 1 for 0,8 e o componente vermelho do vértice 2 for 0,4, usando o modo de sombreamento Gouraud e o modelo de cores RGB, o módulo Direct3D Lighting atribuirá um componente vermelho de 0,6 para o pixel no ponto médio da linha entre esses vértices.</span><span class="sxs-lookup"><span data-stu-id="b8035-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="b8035-122">A ilustração a seguir demonstra o sombreamento Gouraud.</span><span class="sxs-lookup"><span data-stu-id="b8035-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="b8035-123">Esse bule é composto por muitos polígonos simples e triangulares.</span><span class="sxs-lookup"><span data-stu-id="b8035-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="b8035-124">No entanto, o sombreamento de Gouraud faz com que a superfície do objeto pareça curva e suave.</span><span class="sxs-lookup"><span data-stu-id="b8035-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![ilustração de bule usando sombreamento Gouraud](images/gourtea.png)

<span data-ttu-id="b8035-126">O sombreamento de Gouraud também pode ser usado para exibir objetos com bordas nítidas.</span><span class="sxs-lookup"><span data-stu-id="b8035-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="b8035-127">Para obter mais informações, consulte [vetores normais de face e vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="b8035-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8035-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8035-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8035-129">Sombreamento</span><span class="sxs-lookup"><span data-stu-id="b8035-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



