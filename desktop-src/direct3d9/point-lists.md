---
description: Uma lista de ponto é uma coleção de vértices que são renderizados como pontos isolados. Seu aplicativo pode usá-los em cenas 3D para campos de estrela ou linhas pontilhadas na superfície de um polígono.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Listas de pontos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645969"
---
# <a name="point-lists"></a><span data-ttu-id="f748b-104">Listas de pontos</span><span class="sxs-lookup"><span data-stu-id="f748b-104">Point Lists</span></span>

<span data-ttu-id="f748b-105">Uma lista de ponto é uma coleção de vértices que são renderizados como pontos isolados.</span><span class="sxs-lookup"><span data-stu-id="f748b-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="f748b-106">Seu aplicativo pode usá-los em cenas 3D para campos de estrela ou linhas pontilhadas na superfície de um polígono.</span><span class="sxs-lookup"><span data-stu-id="f748b-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="f748b-107">A ilustração a seguir mostra uma lista de ponto renderizada.</span><span class="sxs-lookup"><span data-stu-id="f748b-107">The following illustration depicts a rendered point list.</span></span>

![ilustração de uma lista de ponto](images/pointlst.png)

<span data-ttu-id="f748b-109">Seu app pode aplicar materiais e texturas a uma lista de ponto.</span><span class="sxs-lookup"><span data-stu-id="f748b-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="f748b-110">As cores na textura ou no material aparecem apenas nos pontos desenhados e não entre os pontos.</span><span class="sxs-lookup"><span data-stu-id="f748b-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="f748b-111">O código a seguir mostra como criar vértices para essa lista de pontos.</span><span class="sxs-lookup"><span data-stu-id="f748b-111">The following code shows how to create vertices for this point list.</span></span>


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



<span data-ttu-id="f748b-112">O exemplo de código abaixo mostra como renderizar esta lista de pontos no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="f748b-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="f748b-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f748b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f748b-114">Primitivos</span><span class="sxs-lookup"><span data-stu-id="f748b-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
