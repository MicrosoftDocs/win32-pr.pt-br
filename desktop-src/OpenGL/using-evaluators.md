---
title: Usando avaliadores
description: Usando avaliadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, avaliadores
- avaliadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291990"
---
# <a name="using-evaluators"></a><span data-ttu-id="add47-105">Usando avaliadores</span><span class="sxs-lookup"><span data-stu-id="add47-105">Using Evaluators</span></span>

<span data-ttu-id="add47-106">As funções do avaliador OpenGL permitem usar um mapeamento polinomial para produzir vértices, normais, coordenadas de textura e cores.</span><span class="sxs-lookup"><span data-stu-id="add47-106">The OpenGL evaluator functions allow you to use a polynomial mapping to produce vertices, normals, texture coordinates, and colors.</span></span> <span data-ttu-id="add47-107">Esses valores calculados são passados para o pipeline de processamento como se tivessem sido especificados diretamente.</span><span class="sxs-lookup"><span data-stu-id="add47-107">These calculated values are then passed on to the processing pipeline as if they had been directly specified.</span></span> <span data-ttu-id="add47-108">As funções do avaliador também são a base para as funções NURBS (B não-uniforme racional), que permitem que você defina curvas e superfícies, conforme descrito na [biblioteca do utilitário OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="add47-108">The evaluator functions are also the basis for the NURBS (Non-Uniform Rational B-Spline) functions, which allow you to define curves and surfaces, as described under [OpenGL Utility library](opengl-utility-library.md).</span></span>

<span data-ttu-id="add47-109">A primeira etapa no uso de avaliadores é definir o mapeamento polinomial apropriado de uma ou duas dimensões usando [**glMap \***](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="add47-109">The first step in using evaluators is to define the appropriate one- or two-dimensional polynomial mapping using [**glMap\***](glmap1.md).</span></span> <span data-ttu-id="add47-110">Em seguida, você pode especificar e avaliar os valores de domínio para esse mapa de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="add47-110">You can then specify and evaluate the domain values for this map in one of two ways:</span></span>

-   <span data-ttu-id="add47-111">Defina uma série de valores de domínio com espaçamento uniforme para ser mapeado usando [**glMapGrid**](glmapgrid-functions.md) e, em seguida, avalie um subconjunto retangular dessa grade com [**glEvalMesh**](glevalmesh-functions.md).</span><span class="sxs-lookup"><span data-stu-id="add47-111">Define a series of evenly spaced domain values to be mapped using [**glMapGrid**](glmapgrid-functions.md) and then evaluate a rectangular subset of that grid with [**glEvalMesh**](glevalmesh-functions.md).</span></span> <span data-ttu-id="add47-112">Um único ponto da grade pode ser avaliado usando [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="add47-112">A single point of the grid can be evaluated using [**glEvalPoint**](glevalpoint.md).</span></span>
-   <span data-ttu-id="add47-113">Especifique explicitamente um valor de domínio desejado como um argumento, que avalia os mapas nesse valor.</span><span class="sxs-lookup"><span data-stu-id="add47-113">Explicitly specify a desired domain value as an argument, which evaluates the maps at that value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="add47-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="add47-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add47-115">Referência de avaliadores</span><span class="sxs-lookup"><span data-stu-id="add47-115">Evaluators Reference</span></span>](evaluators-reference.md)
</dt> </dl>

 

 




