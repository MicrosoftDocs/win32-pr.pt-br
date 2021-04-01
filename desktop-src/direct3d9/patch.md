---
description: Define um B&\# 233; patch de controle zier. A matriz define os pontos de controle para o patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825491"
---
# <a name="patch"></a><span data-ttu-id="9f99d-104">Patch</span><span class="sxs-lookup"><span data-stu-id="9f99d-104">Patch</span></span>

<span data-ttu-id="9f99d-105">Define um patch de controle de Bézier.</span><span class="sxs-lookup"><span data-stu-id="9f99d-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="9f99d-106">A matriz define os pontos de controle para o patch.</span><span class="sxs-lookup"><span data-stu-id="9f99d-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="9f99d-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="9f99d-107">Where:</span></span>

-   <span data-ttu-id="9f99d-108">nControlIndices-número de índices de ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="9f99d-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="9f99d-109">array DWORD controlIndices \[ nControlIndices \] -matriz de índices de ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="9f99d-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="9f99d-110">O tipo de patch é definido pelo número de pontos de controle, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f99d-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="9f99d-111">Número de pontos de controle</span><span class="sxs-lookup"><span data-stu-id="9f99d-111">Number of control points</span></span> | <span data-ttu-id="9f99d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f99d-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="9f99d-113">10</span><span class="sxs-lookup"><span data-stu-id="9f99d-113">10</span></span>                       | <span data-ttu-id="9f99d-114">Patch triangular Bézier cúbico</span><span class="sxs-lookup"><span data-stu-id="9f99d-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="9f99d-115">15</span><span class="sxs-lookup"><span data-stu-id="9f99d-115">15</span></span>                       | <span data-ttu-id="9f99d-116">Patch triangular de Bézier quarto</span><span class="sxs-lookup"><span data-stu-id="9f99d-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="9f99d-117">16</span><span class="sxs-lookup"><span data-stu-id="9f99d-117">16</span></span>                       | <span data-ttu-id="9f99d-118">Patch de retângulo quádruplo de Bézier cúbica</span><span class="sxs-lookup"><span data-stu-id="9f99d-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="9f99d-119">A ordem dos pontos de controle é fornecida em um padrão de espiral, conforme mostrado nos diagramas a seguir para patches triangulares e retangulares.</span><span class="sxs-lookup"><span data-stu-id="9f99d-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="9f99d-120">Os patches triangulares usam o padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f99d-120">Triangular patches use the following pattern.</span></span>

![diagrama do padrão para patches triangulares](images/tripatch.png)

<span data-ttu-id="9f99d-122">Os patches retangulares usam o padrão a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f99d-122">Rectangular patches use the following pattern.</span></span>

![diagrama do padrão para patches retangulares](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="9f99d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f99d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f99d-125">Modelos</span><span class="sxs-lookup"><span data-stu-id="9f99d-125">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



