---
description: Uma lista de linhas contém segmentos de linha reta isolados.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Listas de linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105787742"
---
# <a name="line-lists"></a><span data-ttu-id="01bd6-103">Listas de linhas</span><span class="sxs-lookup"><span data-stu-id="01bd6-103">Line Lists</span></span>

<span data-ttu-id="01bd6-104">Uma lista de linhas contém segmentos de linha reta isolados.</span><span class="sxs-lookup"><span data-stu-id="01bd6-104">A line list is a list of isolated, straight line segments.</span></span> <span data-ttu-id="01bd6-105">As listas de linhas são úteis para tarefas como adicionar chuva com neve ou pesada a uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="01bd6-105">Line lists are useful for such tasks as adding sleet or heavy rain to a 3D scene.</span></span> <span data-ttu-id="01bd6-106">Os apps criam uma lista de linhas preenchendo uma matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="01bd6-106">Applications create a line list by filling an array of vertices.</span></span> <span data-ttu-id="01bd6-107">Observe que o número de vértices em uma lista de linhas deve ser um número par maior ou igual a dois.</span><span class="sxs-lookup"><span data-stu-id="01bd6-107">Note that the number of vertices in a line list must be an even number greater than or equal to two.</span></span>

<span data-ttu-id="01bd6-108">A ilustração a seguir mostra uma lista de linha renderizada.</span><span class="sxs-lookup"><span data-stu-id="01bd6-108">The following illustration shows a rendered line list.</span></span>

![Ilustração de uma lista de linhas](images/linelst.png)

<span data-ttu-id="01bd6-110">Você pode aplicar materiais e texturas a uma lista de linhas.</span><span class="sxs-lookup"><span data-stu-id="01bd6-110">You can apply materials and textures to a line list.</span></span> <span data-ttu-id="01bd6-111">As cores no material ou na textura aparecem somente nas linhas desenhadas, não em qualquer ponto entre as linhas.</span><span class="sxs-lookup"><span data-stu-id="01bd6-111">The colors in the material or texture appear only along the lines drawn, not at any point in between the lines.</span></span>

<span data-ttu-id="01bd6-112">O código a seguir mostra como criar vértices para essa lista de linhas.</span><span class="sxs-lookup"><span data-stu-id="01bd6-112">The following code shows how to create vertices for this line list.</span></span>


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



<span data-ttu-id="01bd6-113">O exemplo de código abaixo mostra como renderizar uma lista de linhas no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="01bd6-113">The code example below shows how to render a line list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a><span data-ttu-id="01bd6-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01bd6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01bd6-115">Primitivos</span><span class="sxs-lookup"><span data-stu-id="01bd6-115">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
