---
description: Os aplicativos C++ podem controlar como a neblina afeta a cor dos objetos em uma cena alterando como o Microsoft Direct3D computa efeitos de neblina à distância.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Fórmulas de neblina (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825709"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="44716-103">Fórmulas de neblina (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="44716-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="44716-104">Os aplicativos C++ podem controlar como a neblina afeta a cor dos objetos em uma cena alterando como o Microsoft Direct3D computa efeitos de neblina à distância.</span><span class="sxs-lookup"><span data-stu-id="44716-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="44716-105">O tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) contém membros que identificam as três fórmulas de neblina.</span><span class="sxs-lookup"><span data-stu-id="44716-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="44716-106">Todas as fórmulas calculam um fator de neblina como uma função de distância, determinados parâmetros que seu aplicativo define.</span><span class="sxs-lookup"><span data-stu-id="44716-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="44716-107">Neblina linear</span><span class="sxs-lookup"><span data-stu-id="44716-107">Linear Fog</span></span>

<span data-ttu-id="44716-108">Isso é definido com a equação linear D3DFOG a seguir \_ .</span><span class="sxs-lookup"><span data-stu-id="44716-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![equação da neblina linear do Direct3D](images/fogliner.png)

<span data-ttu-id="44716-110">onde</span><span class="sxs-lookup"><span data-stu-id="44716-110">where</span></span>

-   <span data-ttu-id="44716-111">Start é a distância na qual os efeitos de neblina começam.</span><span class="sxs-lookup"><span data-stu-id="44716-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="44716-112">End é a distância na qual os efeitos de neblina não aumentam mais.</span><span class="sxs-lookup"><span data-stu-id="44716-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="44716-113">d representa profundidade ou distância do ponto de vista.</span><span class="sxs-lookup"><span data-stu-id="44716-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="44716-114">Para a neblina baseada em intervalo, o valor de d é a distância entre a posição da câmera e um vértice.</span><span class="sxs-lookup"><span data-stu-id="44716-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="44716-115">Para a neblina não baseada em intervalo, o valor de d é o valor absoluto da coordenada Z no espaço da câmera.</span><span class="sxs-lookup"><span data-stu-id="44716-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="44716-116">Neblina exponencial</span><span class="sxs-lookup"><span data-stu-id="44716-116">Exponential Fog</span></span>

<span data-ttu-id="44716-117">As fórmulas linear e exponencial têm suporte para sombra de pixel e sombra de vértice.</span><span class="sxs-lookup"><span data-stu-id="44716-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="44716-118">Isso é definido com a equação D3DFOG de exp a seguir \_ .</span><span class="sxs-lookup"><span data-stu-id="44716-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![equação da neblina exponencial do Direct3D](images/fogexp.png)

<span data-ttu-id="44716-120">onde</span><span class="sxs-lookup"><span data-stu-id="44716-120">where</span></span>

-   <span data-ttu-id="44716-121">e é a base de logaritmos naturais (aproximadamente 2,71828).</span><span class="sxs-lookup"><span data-stu-id="44716-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="44716-122">densidade é uma densidade de neblina arbitrária que pode variar de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="44716-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="44716-123">d representa profundidade, ou a distância do ponto de vista, conforme mencionado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="44716-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="44716-124">Isso é definido com a seguinte \_ equação D3DFOG EXP2.</span><span class="sxs-lookup"><span data-stu-id="44716-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![equação da neblina exponencial de Direct3D 2](images/fogexp2.png)

<span data-ttu-id="44716-126">onde</span><span class="sxs-lookup"><span data-stu-id="44716-126">where</span></span>

-   <span data-ttu-id="44716-127">e é a base dos logaritmos naturais, conforme mencionado acima.</span><span class="sxs-lookup"><span data-stu-id="44716-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="44716-128">densidade é uma densidade de neblina arbitrária que pode variar de 0,0 a 1,0, conforme mencionado acima.</span><span class="sxs-lookup"><span data-stu-id="44716-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="44716-129">d representa profundidade, ou a distância do ponto de vista, conforme mencionado acima.</span><span class="sxs-lookup"><span data-stu-id="44716-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="44716-130">O sistema armazena o fator de neblina no componente alfa da cor especular para um vértice.</span><span class="sxs-lookup"><span data-stu-id="44716-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="44716-131">Se seu aplicativo executar sua própria transformação e iluminação, você poderá inserir valores de fator de neblina manualmente, a serem aplicados pelo sistema durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="44716-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="44716-132">O grafo a seguir mostra essas fórmulas, usando valores comuns como nos parâmetros da fórmula.</span><span class="sxs-lookup"><span data-stu-id="44716-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![grafo das fórmulas de neblina ao longo da distância e da quantidade de cores](images/foggraph.png)

<span data-ttu-id="44716-134">D3DFOG \_ linear é 1,0 no início e 0,0 no final.</span><span class="sxs-lookup"><span data-stu-id="44716-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="44716-135">Ele não é medido em relação aos planos próximos ou distantes.</span><span class="sxs-lookup"><span data-stu-id="44716-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="44716-136">Quando o Direct3D calcula os efeitos de neblina, ele usa o fator de neblina de uma das equações anteriores na equação de mesclagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="44716-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![equação de efeitos de neblina para Direct3D](images/fogcalc.png)

<span data-ttu-id="44716-138">Essa fórmula dimensiona efetivamente a cor do polígono C atual pelo fator de neblina f e adiciona o produto à cor de neblina C, dimensionada pelo inverso de bit-a-dia do fator de neblina.</span><span class="sxs-lookup"><span data-stu-id="44716-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="44716-139">O valor de cor resultante é uma mistura da cor da neblina e da cor original, como um fator de distância.</span><span class="sxs-lookup"><span data-stu-id="44716-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="44716-140">A fórmula se aplica a todos os dispositivos com suporte no Microsoft DirectX 7,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="44716-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="44716-141">Para o dispositivo de rampa herdado, o fator de neblina dimensiona os componentes de cores difusas e especulares, clamped para o intervalo de 0,0 e 1,0, inclusive.</span><span class="sxs-lookup"><span data-stu-id="44716-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="44716-142">O fator de neblina normalmente começa em 1,0 para o plano próximo e diminui para 0,0 no plano distante.</span><span class="sxs-lookup"><span data-stu-id="44716-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44716-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44716-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44716-144">Tipos de neblina</span><span class="sxs-lookup"><span data-stu-id="44716-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
