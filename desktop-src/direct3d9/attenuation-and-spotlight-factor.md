---
description: Os componentes de iluminação especular e difusa da equação de iluminação global contêm termos que descrevem a atenuação de luz e o cone em destaque. Esses termos são descritos a seguir.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Fator de atenuação e destaque (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568937"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="858fc-104">Fator de atenuação e destaque (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="858fc-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="858fc-105">Os componentes de iluminação especular e difusa da equação de iluminação global contêm termos que descrevem a atenuação de luz e o cone em destaque.</span><span class="sxs-lookup"><span data-stu-id="858fc-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="858fc-106">Esses termos são descritos a seguir.</span><span class="sxs-lookup"><span data-stu-id="858fc-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="858fc-107">Atenuação</span><span class="sxs-lookup"><span data-stu-id="858fc-107">Attenuation</span></span>

<span data-ttu-id="858fc-108">A atenuação de uma luz depende do tipo de luz e da distância entre a luz e a posição do vértice.</span><span class="sxs-lookup"><span data-stu-id="858fc-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="858fc-109">Para calcular a atenuação, use uma das seguintes equações.</span><span class="sxs-lookup"><span data-stu-id="858fc-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="858fc-110">Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²)</span><span class="sxs-lookup"><span data-stu-id="858fc-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="858fc-111">Em que:</span><span class="sxs-lookup"><span data-stu-id="858fc-111">Where:</span></span>



| <span data-ttu-id="858fc-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="858fc-112">Parameter</span></span>        | <span data-ttu-id="858fc-113">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="858fc-113">Default value</span></span> | <span data-ttu-id="858fc-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="858fc-114">Type</span></span>  | <span data-ttu-id="858fc-115">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="858fc-115">Description</span></span>                                     | <span data-ttu-id="858fc-116">Intervalo</span><span class="sxs-lookup"><span data-stu-id="858fc-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="858fc-117">att0<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-117">att0<sub>i</sub></span></span> | <span data-ttu-id="858fc-118">0.0</span><span class="sxs-lookup"><span data-stu-id="858fc-118">0.0</span></span>           | <span data-ttu-id="858fc-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-119">FLOAT</span></span> | <span data-ttu-id="858fc-120">Fator de atenuação constante</span><span class="sxs-lookup"><span data-stu-id="858fc-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="858fc-121">0 para + infinito</span><span class="sxs-lookup"><span data-stu-id="858fc-121">0 to +infinity</span></span> |
| <span data-ttu-id="858fc-122">att1<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-122">att1<sub>i</sub></span></span> | <span data-ttu-id="858fc-123">0.0</span><span class="sxs-lookup"><span data-stu-id="858fc-123">0.0</span></span>           | <span data-ttu-id="858fc-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-124">FLOAT</span></span> | <span data-ttu-id="858fc-125">Fator de atenuação linear</span><span class="sxs-lookup"><span data-stu-id="858fc-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="858fc-126">0 para + infinito</span><span class="sxs-lookup"><span data-stu-id="858fc-126">0 to +infinity</span></span> |
| <span data-ttu-id="858fc-127">att2<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-127">att2<sub>i</sub></span></span> | <span data-ttu-id="858fc-128">0.0</span><span class="sxs-lookup"><span data-stu-id="858fc-128">0.0</span></span>           | <span data-ttu-id="858fc-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-129">FLOAT</span></span> | <span data-ttu-id="858fc-130">Fator de atenuação quadrática</span><span class="sxs-lookup"><span data-stu-id="858fc-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="858fc-131">0 para + infinito</span><span class="sxs-lookup"><span data-stu-id="858fc-131">0 to +infinity</span></span> |
| <span data-ttu-id="858fc-132">d</span><span class="sxs-lookup"><span data-stu-id="858fc-132">d</span></span>                | <span data-ttu-id="858fc-133">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-133">N/A</span></span>           | <span data-ttu-id="858fc-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-134">FLOAT</span></span> | <span data-ttu-id="858fc-135">Distância da posição de vértice até a posição da luz</span><span class="sxs-lookup"><span data-stu-id="858fc-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="858fc-136">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-136">N/A</span></span>            |



 

-   <span data-ttu-id="858fc-137">Atten = 1, se a luz é uma luz direcional.</span><span class="sxs-lookup"><span data-stu-id="858fc-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="858fc-138">Atten = 0, se a distância entre a luz e o vértice exceder o intervalo da luz.</span><span class="sxs-lookup"><span data-stu-id="858fc-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="858fc-139">Os valores att0, Att1, att2 são especificados pelos membros Attenuation0, Attenuation1 e Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="858fc-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="858fc-140">A distância entre a luz e a posição do vértice é sempre positiva.</span><span class="sxs-lookup"><span data-stu-id="858fc-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="858fc-141">d = \| f<sub>dir</sub>\|</span><span class="sxs-lookup"><span data-stu-id="858fc-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="858fc-142">Em que:</span><span class="sxs-lookup"><span data-stu-id="858fc-142">Where:</span></span>



| <span data-ttu-id="858fc-143">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="858fc-143">Parameter</span></span>       | <span data-ttu-id="858fc-144">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="858fc-144">Default value</span></span> | <span data-ttu-id="858fc-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="858fc-145">Type</span></span>      | <span data-ttu-id="858fc-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="858fc-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="858fc-147">F<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-147">L<sub>dir</sub></span></span> | <span data-ttu-id="858fc-148">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-148">N/A</span></span>           | <span data-ttu-id="858fc-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="858fc-149">D3DVECTOR</span></span> | <span data-ttu-id="858fc-150">Vetor de direção da posição de vértice para a posição da luz</span><span class="sxs-lookup"><span data-stu-id="858fc-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="858fc-151">Se d for maior que o intervalo da luz, ou seja, o membro do intervalo de uma estrutura [**D3DLIGHT9**](d3dlight9.md) , o Direct3D não fará mais cálculos de atenuação e não aplicará nenhum efeito da luz ao vértice.</span><span class="sxs-lookup"><span data-stu-id="858fc-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="858fc-152">As constantes de atenuação atuam como coeficientes na fórmula - você poderá produzir uma variedade de curvas de atenuação fazendo ajustes simples nelas.</span><span class="sxs-lookup"><span data-stu-id="858fc-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="858fc-153">Você pode definir Attenuation1 como 1.0 para criar uma luz sem atenuação, mas que ainda é limitada por intervalo, ou você pode fazer experiências com valores diferentes para obter vários efeitos de atenuação.</span><span class="sxs-lookup"><span data-stu-id="858fc-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="858fc-154">A atenuação no intervalo máximo da luz não é 0.0.</span><span class="sxs-lookup"><span data-stu-id="858fc-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="858fc-155">Para impedir que luzes apareçam repentinamente quando estiverem no intervalo de luz, um app pode aumentar o intervalo de luz.</span><span class="sxs-lookup"><span data-stu-id="858fc-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="858fc-156">Ou então, o app pode configurar constantes de atenuação para que o fator de atenuação fique próximo de 0.0 no intervalo de luz.</span><span class="sxs-lookup"><span data-stu-id="858fc-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="858fc-157">O valor de atenuação é multiplicado pelos componentes em vermelho, verde e azul de cor da luz para dimensionar a intensidade da luz, à medida que um fator de luz de distância transita para um vértice.</span><span class="sxs-lookup"><span data-stu-id="858fc-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="858fc-158">Fator de destaque</span><span class="sxs-lookup"><span data-stu-id="858fc-158">Spotlight Factor</span></span>

<span data-ttu-id="858fc-159">A seguinte equação especifica o fator de destaque.</span><span class="sxs-lookup"><span data-stu-id="858fc-159">The following equation specifies the spotlight factor.</span></span>

![equação de fator de destaque](images/dx8light9.png)



| <span data-ttu-id="858fc-161">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="858fc-161">Parameter</span></span>         | <span data-ttu-id="858fc-162">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="858fc-162">Default value</span></span> | <span data-ttu-id="858fc-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="858fc-163">Type</span></span>  | <span data-ttu-id="858fc-164">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="858fc-164">Description</span></span>                              | <span data-ttu-id="858fc-165">Intervalo</span><span class="sxs-lookup"><span data-stu-id="858fc-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="858fc-166">Rô<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="858fc-167">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-167">N/A</span></span>           | <span data-ttu-id="858fc-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-168">FLOAT</span></span> | <span data-ttu-id="858fc-169">cosseno(ângulo) para destaque i</span><span class="sxs-lookup"><span data-stu-id="858fc-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="858fc-170">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-170">N/A</span></span>                      |
| <span data-ttu-id="858fc-171">phi<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="858fc-172">0.0</span><span class="sxs-lookup"><span data-stu-id="858fc-172">0.0</span></span>           | <span data-ttu-id="858fc-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-173">FLOAT</span></span> | <span data-ttu-id="858fc-174">Ângulo de penumbra de destaque i em radianos</span><span class="sxs-lookup"><span data-stu-id="858fc-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="858fc-175">\[teta<sub>i</sub>, PI)</span><span class="sxs-lookup"><span data-stu-id="858fc-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="858fc-176">teta<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-176">theta<sub>i</sub></span></span> | <span data-ttu-id="858fc-177">0.0</span><span class="sxs-lookup"><span data-stu-id="858fc-177">0.0</span></span>           | <span data-ttu-id="858fc-178">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-178">FLOAT</span></span> | <span data-ttu-id="858fc-179">Ângulo de penumbra de destaque i em radianos</span><span class="sxs-lookup"><span data-stu-id="858fc-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="858fc-180">\[0, PI)</span><span class="sxs-lookup"><span data-stu-id="858fc-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="858fc-181">queda</span><span class="sxs-lookup"><span data-stu-id="858fc-181">falloff</span></span>           | <span data-ttu-id="858fc-182">0.0</span><span class="sxs-lookup"><span data-stu-id="858fc-182">0.0</span></span>           | <span data-ttu-id="858fc-183">FLOAT</span><span class="sxs-lookup"><span data-stu-id="858fc-183">FLOAT</span></span> | <span data-ttu-id="858fc-184">Fator de queda</span><span class="sxs-lookup"><span data-stu-id="858fc-184">Falloff factor</span></span>                           | <span data-ttu-id="858fc-185">(-infinito + infinito)</span><span class="sxs-lookup"><span data-stu-id="858fc-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="858fc-186">Em que:</span><span class="sxs-lookup"><span data-stu-id="858fc-186">Where:</span></span>

<span data-ttu-id="858fc-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="858fc-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="858fc-188">e:</span><span class="sxs-lookup"><span data-stu-id="858fc-188">and:</span></span>



| <span data-ttu-id="858fc-189">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="858fc-189">Parameter</span></span>       | <span data-ttu-id="858fc-190">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="858fc-190">Default value</span></span> | <span data-ttu-id="858fc-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="858fc-191">Type</span></span>      | <span data-ttu-id="858fc-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="858fc-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="858fc-193"><sub>DCS</sub> do L</span><span class="sxs-lookup"><span data-stu-id="858fc-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="858fc-194">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-194">N/A</span></span>           | <span data-ttu-id="858fc-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="858fc-195">D3DVECTOR</span></span> | <span data-ttu-id="858fc-196">O negativo da direção da luz no espaço da câmera</span><span class="sxs-lookup"><span data-stu-id="858fc-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="858fc-197">F<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="858fc-197">L<sub>dir</sub></span></span> | <span data-ttu-id="858fc-198">N/D</span><span class="sxs-lookup"><span data-stu-id="858fc-198">N/A</span></span>           | <span data-ttu-id="858fc-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="858fc-199">D3DVECTOR</span></span> | <span data-ttu-id="858fc-200">Vetor de direção da posição de vértice para a posição da luz</span><span class="sxs-lookup"><span data-stu-id="858fc-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="858fc-201">Depois de computar a atenuação de luz, o Direct3D também considera os efeitos de destaque, se aplicável, o ângulo que a luz reflete de uma superfície e a reflexão do material atual para calcular os componentes difuso e especular para esse vértice.</span><span class="sxs-lookup"><span data-stu-id="858fc-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="858fc-202">Para obter mais informações, consulte [Spotlight](light-types.md).</span><span class="sxs-lookup"><span data-stu-id="858fc-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="858fc-203">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="858fc-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="858fc-204">Matemática de iluminação</span><span class="sxs-lookup"><span data-stu-id="858fc-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



