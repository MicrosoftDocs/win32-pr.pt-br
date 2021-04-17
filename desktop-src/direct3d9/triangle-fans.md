---
description: Um ventilador de triângulo é semelhante a uma faixa de triângulo, exceto pelo fato de que todos os triângulos compartilham um vértice, conforme mostrado na ilustração a seguir.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventiladores de triângulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559253"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="ae748-103">Ventiladores de triângulo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ae748-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="ae748-104">Um ventilador de triângulo é semelhante a uma faixa de triângulo, exceto pelo fato de que todos os triângulos compartilham um vértice, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae748-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![ilustração de um ventilador de triângulo](images/trifan.gif)

<span data-ttu-id="ae748-106">O sistema usa os vértices v2, v3 e V1 para desenhar o primeiro triângulo; V3, v4 e V1 para desenhar o segundo triângulo; v4, v5 e V1 para desenhar o terceiro triângulo; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ae748-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="ae748-107">Quando o sombreamento simples é habilitado, o sistema sombreia o triângulo com a cor de seu primeiro vértice.</span><span class="sxs-lookup"><span data-stu-id="ae748-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="ae748-108">A ilustração a seguir mostra um ventilador de triângulo renderizado.</span><span class="sxs-lookup"><span data-stu-id="ae748-108">The following illustration depicts a rendered triangle fan.</span></span>

![ilustração de um ventilador de triângulo renderizado](images/tfan2.gif)

<span data-ttu-id="ae748-110">O código a seguir mostra como criar vértices para este ventilador de triângulo.</span><span class="sxs-lookup"><span data-stu-id="ae748-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="ae748-111">O exemplo de código abaixo mostra como renderizar esse ventilador de triângulo no Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="ae748-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="ae748-112">Não há suporte para ventiladores de triângulo no Direct3D 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ae748-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae748-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae748-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae748-114">Primitivos</span><span class="sxs-lookup"><span data-stu-id="ae748-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
