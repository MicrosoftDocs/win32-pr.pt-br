---
title: Tendência de profundidade
description: Polígonos que são coplanar no espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z (ou uma tendência de profundidade) a cada um.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103643008"
---
# <a name="depth-bias"></a><span data-ttu-id="639bc-103">Tendência de profundidade</span><span class="sxs-lookup"><span data-stu-id="639bc-103">Depth Bias</span></span>

<span data-ttu-id="639bc-104">Polígonos que são coplanar no espaço 3D podem ser feitos para aparecer como se não fossem coplanar adicionando um Bias z (ou uma tendência de profundidade) a cada um.</span><span class="sxs-lookup"><span data-stu-id="639bc-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="639bc-105">Essa é uma técnica comumente usada para garantir que as sombras em uma cena sejam exibidas corretamente.</span><span class="sxs-lookup"><span data-stu-id="639bc-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="639bc-106">Por exemplo, uma sombra em uma parede provavelmente terá o mesmo valor de profundidade que a parede.</span><span class="sxs-lookup"><span data-stu-id="639bc-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="639bc-107">Se um aplicativo renderizar uma parede primeiro e, em seguida, uma sombra, a sombra pode não estar visível ou os artefatos de profundidade podem estar visíveis.</span><span class="sxs-lookup"><span data-stu-id="639bc-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="639bc-108">Um aplicativo pode ajudar a garantir que polígonos coplanar sejam renderizados corretamente adicionando a tendência (do membro **DepthBias** do [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) aos valores z que o sistema usa ao renderizar os conjuntos de polígonos de coplanar.</span><span class="sxs-lookup"><span data-stu-id="639bc-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="639bc-109">Polígonos com um valor z maior serão desenhados na frente de polígonos com um valor z menor.</span><span class="sxs-lookup"><span data-stu-id="639bc-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="639bc-110">Há duas opções para calcular a tendência de profundidade.</span><span class="sxs-lookup"><span data-stu-id="639bc-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="639bc-111">Se o buffer de profundidade atualmente associado ao estágio output-merger tiver um formato **UNORM** ou nenhum buffer de profundidade estiver associado, o valor de tendência será calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="639bc-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="639bc-112">em que *r* é o valor mínimo representável > 0 no formato de buffer de profundidade convertido em **float32**.</span><span class="sxs-lookup"><span data-stu-id="639bc-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="639bc-113">Os valores **DepthBias** e **SlopeScaledDepthBias** são membros da estrutura [**\_ \_ DESC1 do rasterizador D3D11**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) .</span><span class="sxs-lookup"><span data-stu-id="639bc-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="639bc-114">O valor de **MaxDepthSlope** é o máximo dos declives horizontal e vertical do valor de profundidade no pixel.</span><span class="sxs-lookup"><span data-stu-id="639bc-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="639bc-115">Se um buffer de profundidade de ponto flutuante estiver associado ao estágio de mesclagem de saída, o valor de tendência será calculado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="639bc-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="639bc-116">em que *r* é o número de bits mantissa na representação de ponto flutuante (excluindo o bit oculto); por exemplo, 23 para **float32**.</span><span class="sxs-lookup"><span data-stu-id="639bc-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="639bc-117">O valor de tendência é então clamped assim:</span><span class="sxs-lookup"><span data-stu-id="639bc-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="639bc-118">Em seguida, o valor de tendência é usado para calcular a profundidade de pixels.</span><span class="sxs-lookup"><span data-stu-id="639bc-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="639bc-119">As operações de tendência de profundidade ocorrem em vértices após o recorte, portanto, a diferença de profundidade não tem efeito no recorte geométrico.</span><span class="sxs-lookup"><span data-stu-id="639bc-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="639bc-120">O valor de tendência é constante para um determinado primitivo e é adicionado ao valor z para cada vértice antes da configuração do interpolador.</span><span class="sxs-lookup"><span data-stu-id="639bc-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="639bc-121">Quando você usa [os níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 e superior, todos os cálculos de tendência são executados usando aritmética de ponto flutuante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="639bc-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="639bc-122">A tendência não é aplicada a primitivas de ponto ou de linha, exceto para linhas desenhadas no modo de wireframe.</span><span class="sxs-lookup"><span data-stu-id="639bc-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="639bc-123">Um dos artefatos com sombras com base no buffer de sombra é o acne de sombra ou um sombreamento de superfície em si devido a pequenas diferenças entre a computação de profundidade em um sombreador e a profundidade da mesma superfície no buffer de sombra.</span><span class="sxs-lookup"><span data-stu-id="639bc-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="639bc-124">Uma maneira de aliviar isso é usar **DepthBias** e **SlopeScaledDepthBias** ao renderizar um buffer de sombra.</span><span class="sxs-lookup"><span data-stu-id="639bc-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="639bc-125">A ideia é distribuir as superfícies o suficiente ao renderizar um buffer de sombra para que o resultado da comparação (entre o buffer de sombra z e o sombreador z) seja consistente em toda a superfície e evite a autosombra local.</span><span class="sxs-lookup"><span data-stu-id="639bc-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="639bc-126">No entanto, usar **DepthBias** e **SlopeScaledDepthBias** pode introduzir novos problemas de renderização quando um polígono exibido em um ângulo extremamente nítido faz com que a equação de tendência gere um valor z muito grande.</span><span class="sxs-lookup"><span data-stu-id="639bc-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="639bc-127">Isso, em vigor, envia o polígono extremamente longe da superfície original no mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="639bc-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="639bc-128">Uma maneira de ajudar a aliviar esse problema específico é usar o **DepthBiasClamp**, que fornece um limite superior (positivo ou negativo) na magnitude da diferença de z calculada.</span><span class="sxs-lookup"><span data-stu-id="639bc-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="639bc-129">Para [os níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="639bc-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="639bc-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="639bc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="639bc-131">Estágio de fusão de saída</span><span class="sxs-lookup"><span data-stu-id="639bc-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




