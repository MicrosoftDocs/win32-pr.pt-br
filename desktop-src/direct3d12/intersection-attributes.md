---
title: Estrutura de atributos de interseção
description: Uma estrutura declarada em HLSL para representar os atributos de acesso para a interseção de triângulo de função fixa ou a caixa delimitadora alinhada por eixo para a interseção de procedimento primitivo.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "105798230"
---
# <a name="intersection-attributes-structure"></a><span data-ttu-id="b19c9-103">Estrutura de atributos de interseção</span><span class="sxs-lookup"><span data-stu-id="b19c9-103">Intersection attributes structure</span></span> 

<span data-ttu-id="b19c9-104">Uma estrutura declarada em HLSL para representar os atributos de acesso para a interseção de triângulo de função fixa ou a caixa delimitadora alinhada por eixo para a interseção de procedimento primitivo.</span><span class="sxs-lookup"><span data-stu-id="b19c9-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="b19c9-105">Interseção de triângulo de função fixa</span><span class="sxs-lookup"><span data-stu-id="b19c9-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="b19c9-106">A seguinte estrutura é declarada em HLSL para representar os atributos de acesso para a interseção de triângulo de função fixa:</span><span class="sxs-lookup"><span data-stu-id="b19c9-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="b19c9-107">[Quaisquer pressionamentos](any-hit-shader.md) de tecla de acesso e [mais próximos](closest-hit-shader.md) invocados usando a interseção de triângulo de função fixa devem usar essa estrutura para os atributos de pressionamento.</span><span class="sxs-lookup"><span data-stu-id="b19c9-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="b19c9-108">Determinados atributos a0, a1 e a2 para os 3 vértices de um triângulo, barycentrics. x é o peso para a1 e barycentrics. y é o peso de a2.</span><span class="sxs-lookup"><span data-stu-id="b19c9-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="b19c9-109">Por exemplo, o aplicativo pode se interpolar fazendo: a = a0 + barycentrics. x \* (a1-a0) + barycentrics. y \* (a2 – a0).</span><span class="sxs-lookup"><span data-stu-id="b19c9-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="b19c9-110">Caixa delimitadora alinhada ao eixo para a interseção de procedimento primitivo</span><span class="sxs-lookup"><span data-stu-id="b19c9-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="b19c9-111">Quando caixas delimitadores alinhadas por eixo são usadas para interseção com primitivos de procedimento, um sombreador de interseção é disparado.</span><span class="sxs-lookup"><span data-stu-id="b19c9-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="b19c9-112">Esse sombreador fornece uma estrutura de atributo de interseção definida pelo usuário para a chamada [**ReportHit**](reporthit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="b19c9-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="b19c9-113">Os sombreadores de pressionamento de qualquer clique e mais próximo vinculados no mesmo grupo de acesso com esse sombreador de interseção devem usar a mesma estrutura para atributos de pressionamento, mesmo que os atributos não sejam referenciados.</span><span class="sxs-lookup"><span data-stu-id="b19c9-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="b19c9-114">O tamanho máximo da estrutura de atributo é 32 bytes, definido como **D3D12 \_ RAYTRACING \_ \_ tamanho máximo \_ do atributo \_ em \_ bytes**.</span><span class="sxs-lookup"><span data-stu-id="b19c9-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


