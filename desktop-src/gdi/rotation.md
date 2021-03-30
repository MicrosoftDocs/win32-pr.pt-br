---
description: Muitos aplicativos CAD fornecem recursos que giram objetos desenhados na área do cliente.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968182"
---
# <a name="rotation"></a><span data-ttu-id="2f865-103">Rotação</span><span class="sxs-lookup"><span data-stu-id="2f865-103">Rotation</span></span>

<span data-ttu-id="2f865-104">Muitos aplicativos CAD fornecem recursos que giram objetos desenhados na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="2f865-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="2f865-105">Aplicativos que incluem recursos de rotação usam a função [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para definir o espaço mundial apropriado para a transformação de espaço em página.</span><span class="sxs-lookup"><span data-stu-id="2f865-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="2f865-106">Essa função recebe um ponteiro para uma estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) que contém os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="2f865-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="2f865-107">Os membros eM11, eM12, eM21 e eM22 do XFORM especificam, respectivamente, o cosseno, o seno, o seno negativo e o cosseno do ângulo de rotação.</span><span class="sxs-lookup"><span data-stu-id="2f865-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="2f865-108">Quando a *rotação* ocorre, os pontos que constituem um objeto são girados em relação à origem do espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="2f865-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="2f865-109">A ilustração a seguir mostra um retângulo de 20 a 20 unidades girado em 30 graus quando copiado do espaço de coordenadas mundiais para o espaço de coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="2f865-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![ilustração mostrando dois espaços de coordenadas; cada um tem um retângulo em um local diferente e com uma rotação diferente](images/cstrn-11.png)

<span data-ttu-id="2f865-111">Na ilustração anterior, cada ponto no retângulo foi girado em 30 graus em relação à origem do espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="2f865-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="2f865-112">O algoritmo a seguir computa a nova coordenada x (x ') para um ponto (x, y) que é girado pelo ângulo A com relação à origem do espaço de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="2f865-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="2f865-113">O algoritmo a seguir computa a coordenada y (y) para um ponto (x, y) que é girado pelo ângulo a em relação à origem.</span><span class="sxs-lookup"><span data-stu-id="2f865-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="2f865-114">As duas transformações de rotação podem ser combinadas em uma matriz 2-por-2 da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="2f865-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="2f865-115">A matriz 2-por-2 que produziu a rotação contém os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f865-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="2f865-116">Derivação de algoritmo de rotação</span><span class="sxs-lookup"><span data-stu-id="2f865-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="2f865-117">Os algoritmos de rotação são baseados na teorema de adição de trigonometria, informando que a função trigonométrica de uma soma de dois ângulos (a1 e a2) pode ser expressa em termos das funções trigonométricas dos dois ângulos.</span><span class="sxs-lookup"><span data-stu-id="2f865-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="2f865-118">A ilustração a seguir mostra um ponto no sentido anti-horário girado para uma nova posição p '.</span><span class="sxs-lookup"><span data-stu-id="2f865-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="2f865-119">Além disso, ele mostra dois triângulos formados por uma linha desenhada da origem de espaço de coordenadas para cada ponto e uma linha desenhada de cada ponto através do eixo x.</span><span class="sxs-lookup"><span data-stu-id="2f865-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![diagrama mostrando a origem, p e p e dois triângulos](images/cstrn-12.png)

<span data-ttu-id="2f865-121">Usando trigonometria, a coordenada x do ponto p pode ser obtida multiplicando o comprimento do hipotenusa h pelo cosseno de a1.</span><span class="sxs-lookup"><span data-stu-id="2f865-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="2f865-122">A coordenada y do ponto p pode ser obtida multiplicando-se o comprimento do hipotenusa h pelo seno de a1.</span><span class="sxs-lookup"><span data-stu-id="2f865-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="2f865-123">Da mesma forma, a coordenada x do ponto p ' pode ser obtida multiplicando o comprimento do hipotenusa h pelo cosseno de (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="2f865-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="2f865-124">Por fim, a coordenada y do ponto p ' pode ser obtida multiplicando o comprimento do hipotenusa h pelo seno de (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="2f865-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="2f865-125">Usando o teorema de adição, os algoritmos anteriores se tornam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2f865-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="2f865-126">Os algoritmos de rotação para um determinado ponto girados por ângulo a2 podem ser obtidos substituindo x para cada ocorrência de (h \* cos a1) e substituindo y por cada ocorrência de (h \* sin a1).</span><span class="sxs-lookup"><span data-stu-id="2f865-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



