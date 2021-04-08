---
description: Para entender totalmente um sombreador que implementa o PRT, é útil derivar a fórmula usada pelo sombreador para calcular Exit radiante.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Equações de PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087705"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="538cd-103">Equações de PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="538cd-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="538cd-104">Para entender totalmente um sombreador que implementa o PRT, é útil derivar a fórmula usada pelo sombreador para calcular Exit radiante.</span><span class="sxs-lookup"><span data-stu-id="538cd-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="538cd-105">Para começar, a equação a seguir é a equação geral para calcular o radiante de saída resultante da iluminação direta em um objeto difuso com iluminação distante arbitrária.</span><span class="sxs-lookup"><span data-stu-id="538cd-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![equação da radiante de saída resultante da iluminação direta em um objeto difuso com iluminação distante arbitrária](images/prt-theory-eq1.png)

<span data-ttu-id="538cd-107">em que:</span><span class="sxs-lookup"><span data-stu-id="538cd-107">where:</span></span>



| <span data-ttu-id="538cd-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="538cd-108">Parameter</span></span>     | <span data-ttu-id="538cd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="538cd-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="538cd-110">RP</span><span class="sxs-lookup"><span data-stu-id="538cd-110">Rₚ</span></span>            | <span data-ttu-id="538cd-111">O radiante de saída no vértice p.</span><span class="sxs-lookup"><span data-stu-id="538cd-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="538cd-112">Avaliado em cada vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="538cd-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="538cd-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="538cd-113">p<sub>d</sub></span></span> | <span data-ttu-id="538cd-114">O albedo da superfície.</span><span class="sxs-lookup"><span data-stu-id="538cd-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="538cd-115">pi</span><span class="sxs-lookup"><span data-stu-id="538cd-115">pi</span></span>            | <span data-ttu-id="538cd-116">Uma constante, usada como um fator de normalização de conservação de energia.</span><span class="sxs-lookup"><span data-stu-id="538cd-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="538cd-117">L (s)</span><span class="sxs-lookup"><span data-stu-id="538cd-117">L(s)</span></span>          | <span data-ttu-id="538cd-118">O ambiente de iluminação (radiante de origem).</span><span class="sxs-lookup"><span data-stu-id="538cd-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="538cd-119">VP de ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="538cd-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="538cd-120">Uma função de visibilidade binária para o ponto p.</span><span class="sxs-lookup"><span data-stu-id="538cd-120">A binary visibility function for point p.</span></span> <span data-ttu-id="538cd-121">Será 1 se o ponto puder ver a luz, 0 se não for.</span><span class="sxs-lookup"><span data-stu-id="538cd-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="538cd-122">HNP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="538cd-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="538cd-123">O termo do cosseno da lei do Lambert.</span><span class="sxs-lookup"><span data-stu-id="538cd-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="538cd-124">Igual a Max ((NP · s), 0), em que NP é a superfície normal no ponto p.</span><span class="sxs-lookup"><span data-stu-id="538cd-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="538cd-125">s</span><span class="sxs-lookup"><span data-stu-id="538cd-125">s</span></span>             | <span data-ttu-id="538cd-126">A variável que se integra à esfera.</span><span class="sxs-lookup"><span data-stu-id="538cd-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="538cd-127">Usando funções de base esféricas, como harmônicas esféricas, a equação a seguir aproxima o ambiente de iluminação.</span><span class="sxs-lookup"><span data-stu-id="538cd-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![equação do ambiente de iluminação](images/prt-theory-eq2.png)

<span data-ttu-id="538cd-129">em que:</span><span class="sxs-lookup"><span data-stu-id="538cd-129">where:</span></span>



| <span data-ttu-id="538cd-130">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="538cd-130">Parameter</span></span>        | <span data-ttu-id="538cd-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="538cd-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="538cd-132">L (s)</span><span class="sxs-lookup"><span data-stu-id="538cd-132">L(s)</span></span>             | <span data-ttu-id="538cd-133">O ambiente de iluminação (radiante de origem).</span><span class="sxs-lookup"><span data-stu-id="538cd-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="538cd-134">i</span><span class="sxs-lookup"><span data-stu-id="538cd-134">i</span></span>                | <span data-ttu-id="538cd-135">Um inteiro que soma o número de funções de base.</span><span class="sxs-lookup"><span data-stu-id="538cd-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="538cd-136">O</span><span class="sxs-lookup"><span data-stu-id="538cd-136">O</span></span>                | <span data-ttu-id="538cd-137">A ordem das harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="538cd-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="538cd-138">l<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="538cd-138">l<sub>i</sub></span></span>    | <span data-ttu-id="538cd-139">Um coeficiente.</span><span class="sxs-lookup"><span data-stu-id="538cd-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="538cd-140">Y<sub>i (s)</sub></span><span class="sxs-lookup"><span data-stu-id="538cd-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="538cd-141">Uma função base sobre a esfera.</span><span class="sxs-lookup"><span data-stu-id="538cd-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="538cd-142">A coleção desses coeficientes, L ', fornece a aproximação ideal para a função L (s) com as funções de base Y (s).</span><span class="sxs-lookup"><span data-stu-id="538cd-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="538cd-143">A substituição e a distribuição produz a equação a seguir.</span><span class="sxs-lookup"><span data-stu-id="538cd-143">Substituting and distributing yields the following equation.</span></span>

![equação do radiante de saída depois de substituir l (s) e distribuir](images/prt-theory-eq3.png)

<span data-ttu-id="538cd-145">O integral de Y<sub>i (s)</sub>VP de ₍ s ₎ HNP ₍ s ₎ é um coeficiente de transferência t<sub>PI</sub> que o simulador computa para cada vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="538cd-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="538cd-146">Substituir isso produz a equação a seguir.</span><span class="sxs-lookup"><span data-stu-id="538cd-146">Substituting this yields the following equation.</span></span>

![equação do radiante de saída depois de substituir o coeficiente de transferência](images/prt-theory-eq4.png)

<span data-ttu-id="538cd-148">A alteração dessa notação de vetor produz a seguinte equação descompactada para calcular a saída radiante para cada canal.</span><span class="sxs-lookup"><span data-stu-id="538cd-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![equação da radiante de saída após alterar para notação de vetor](images/prt-theory-eq5.png)

<span data-ttu-id="538cd-150">em que:</span><span class="sxs-lookup"><span data-stu-id="538cd-150">where:</span></span>



| <span data-ttu-id="538cd-151">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="538cd-151">Parameter</span></span>     | <span data-ttu-id="538cd-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="538cd-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="538cd-153">RP</span><span class="sxs-lookup"><span data-stu-id="538cd-153">Rₚ</span></span>            | <span data-ttu-id="538cd-154">O radiante de saída no vértice p.</span><span class="sxs-lookup"><span data-stu-id="538cd-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="538cd-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="538cd-155">p<sub>d</sub></span></span> | <span data-ttu-id="538cd-156">O albedo da superfície.</span><span class="sxs-lookup"><span data-stu-id="538cd-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="538cd-157">Debug</span><span class="sxs-lookup"><span data-stu-id="538cd-157">L'</span></span>            | <span data-ttu-id="538cd-158">O vetor de l<sub>i</sub>e é a projeção do radiante de origem nas funções de base harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="538cd-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="538cd-159">Este é um vetor do pedido ² de coeficientes de harmônica esférica.</span><span class="sxs-lookup"><span data-stu-id="538cd-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="538cd-160">TP</span><span class="sxs-lookup"><span data-stu-id="538cd-160">Tₚ</span></span>            | <span data-ttu-id="538cd-161">Um vetor de transferência do pedido ² para o vértice p.</span><span class="sxs-lookup"><span data-stu-id="538cd-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="538cd-162">O simulador divide os coeficientes de transferência por p.</span><span class="sxs-lookup"><span data-stu-id="538cd-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="538cd-163">Esses dois vetores são um vetor de pedido ² de coeficientes de harmônica esférica, portanto, observe que esse é simplesmente um produto de ponto.</span><span class="sxs-lookup"><span data-stu-id="538cd-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="538cd-164">Dependendo da ordem, o ponto pode ser caro, portanto, a compactação pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="538cd-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="538cd-165">Um algoritmo chamado análise de componente principal clusterizado (CPCA) compacta os dados com eficiência.</span><span class="sxs-lookup"><span data-stu-id="538cd-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="538cd-166">Isso permite o uso de uma aproximação harmônica esférica de ordem superior, que resulta em sombras mais nítidas.</span><span class="sxs-lookup"><span data-stu-id="538cd-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="538cd-167">O CPCA fornece a equação a seguir para aproximar o vetor de transferência.</span><span class="sxs-lookup"><span data-stu-id="538cd-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![equação do vetor de transferência aproximado](images/prt-theory-eq6.png)

<span data-ttu-id="538cd-169">em que:</span><span class="sxs-lookup"><span data-stu-id="538cd-169">where:</span></span>



| <span data-ttu-id="538cd-170">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="538cd-170">Parameter</span></span>      | <span data-ttu-id="538cd-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="538cd-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="538cd-172">TP</span><span class="sxs-lookup"><span data-stu-id="538cd-172">Tₚ</span></span>             | <span data-ttu-id="538cd-173">O vetor de transferência para o vértice p.</span><span class="sxs-lookup"><span data-stu-id="538cd-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="538cd-174">MK</span><span class="sxs-lookup"><span data-stu-id="538cd-174">Mₖ</span></span>             | <span data-ttu-id="538cd-175">A média do cluster k.</span><span class="sxs-lookup"><span data-stu-id="538cd-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="538cd-176">j</span><span class="sxs-lookup"><span data-stu-id="538cd-176">j</span></span>              | <span data-ttu-id="538cd-177">Um inteiro que soma o número de vetores do PCA.</span><span class="sxs-lookup"><span data-stu-id="538cd-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="538cd-178">N</span><span class="sxs-lookup"><span data-stu-id="538cd-178">N</span></span>              | <span data-ttu-id="538cd-179">O número de vetores do PCA.</span><span class="sxs-lookup"><span data-stu-id="538cd-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="538cd-180">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="538cd-180">w<sub>pj</sub></span></span> | <span data-ttu-id="538cd-181">O peso do PCA jth para o ponto p.</span><span class="sxs-lookup"><span data-stu-id="538cd-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="538cd-182">B<sub>KJ</sub></span><span class="sxs-lookup"><span data-stu-id="538cd-182">B<sub>kj</sub></span></span> | <span data-ttu-id="538cd-183">O vetor de base do PCA do jth para o cluster k.</span><span class="sxs-lookup"><span data-stu-id="538cd-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="538cd-184">Um cluster é simplesmente um número de vértices que compartilham o mesmo vetor médio.</span><span class="sxs-lookup"><span data-stu-id="538cd-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="538cd-185">Como obter a média do cluster, os pesos do PCA, os vetores de base do PCA e as IDs de cluster para os vértices são discutidos abaixo.</span><span class="sxs-lookup"><span data-stu-id="538cd-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="538cd-186">A substituição dessas duas equações gera:</span><span class="sxs-lookup"><span data-stu-id="538cd-186">Substituting these two equations yields:</span></span>

![equação do radiante de saída depois de substituir o vetor de transferência](images/prt-theory-eq7.png)

<span data-ttu-id="538cd-188">Em seguida, a distribuição do produto dot produz a equação a seguir.</span><span class="sxs-lookup"><span data-stu-id="538cd-188">Then distributing the dot product yields the following equation.</span></span>

![equação do radiante de saída após a distribuição do produto dot](images/prt-theory-eq8.png)

<span data-ttu-id="538cd-190">Porque ambos (MK · L ') e (B<sub>KJ</sub>· L ') são constantes por vértice, o exemplo calcula esses valores com a CPU e os passa como constantes para o sombreador de vértice; como w<sub>PJ</sub> muda para cada vértice, o exemplo armazena esses dados por vértice no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="538cd-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="538cd-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="538cd-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="538cd-192">Transferência de radiante preputada</span><span class="sxs-lookup"><span data-stu-id="538cd-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



