---
description: Uma faixa de linhas é um primitivo composto de segmentos de linha conectados.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Faixas de linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500525"
---
# <a name="line-strips"></a><span data-ttu-id="54f9c-103">Faixas de linha</span><span class="sxs-lookup"><span data-stu-id="54f9c-103">Line Strips</span></span>

<span data-ttu-id="54f9c-104">Uma faixa de linhas é um primitivo composto de segmentos de linha conectados.</span><span class="sxs-lookup"><span data-stu-id="54f9c-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="54f9c-105">O app pode usar faixas de linhas para criar polígonos não fechados.</span><span class="sxs-lookup"><span data-stu-id="54f9c-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="54f9c-106">Um polígono fechado tem o último vértice conectado ao primeiro por um segmento de linhas.</span><span class="sxs-lookup"><span data-stu-id="54f9c-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="54f9c-107">Se o app faz polígonos com base em faixas alinhadas, os vértices não têm garantia de estar coplanares.</span><span class="sxs-lookup"><span data-stu-id="54f9c-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="54f9c-108">A ilustração a seguir mostra uma faixa de linhas renderizada.</span><span class="sxs-lookup"><span data-stu-id="54f9c-108">The following illustration shows a rendered line strip.</span></span>

![Ilustração de uma faixa de linhas](images/linstrip.gif)

<span data-ttu-id="54f9c-110">O código a seguir mostra como criar vértices para essa faixa de linhas.</span><span class="sxs-lookup"><span data-stu-id="54f9c-110">The following code shows how to create vertices for this line strip.</span></span>


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



<span data-ttu-id="54f9c-111">O exemplo de código abaixo mostra como renderizar uma faixa de linha no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="54f9c-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="54f9c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54f9c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54f9c-113">Primitivos</span><span class="sxs-lookup"><span data-stu-id="54f9c-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
