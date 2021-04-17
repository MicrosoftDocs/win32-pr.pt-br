---
description: Transferência radiante de computação (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transferência radiante de computação (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556691"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="f2aa3-103">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f2aa3-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="f2aa3-104">Usando a transferência radiante precomputada</span><span class="sxs-lookup"><span data-stu-id="f2aa3-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="f2aa3-105">Há várias formas de complexidade presentes em cenas interessantes, incluindo como o ambiente de iluminação é modelado (ou seja, modelos de iluminação de área versus pontos/direcionais) e que tipo de efeitos globais são modelados (por exemplo, sombras, interflexões, dispersão de subsuperfície). As técnicas tradicionais de renderização interativa modelam um valor limitado dessa complexidade.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="f2aa3-106">O PRT habilita esses efeitos com algumas restrições significativas:</span><span class="sxs-lookup"><span data-stu-id="f2aa3-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="f2aa3-107">Os objetos são considerados rígidos (ou seja, sem deformações).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="f2aa3-108">É uma abordagem centrada no objeto (a menos que os objetos sejam movidos juntos, esses efeitos globais não são mantidos entre eles).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="f2aa3-109">Apenas iluminação de baixa frequência é modelada (resultando em sombras suaves). Para luzes de alta frequência (sombras nítidas), as técnicas tradicionais teriam de ser empregadas.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="f2aa3-110">O PRT requer um dos seguintes, mas não ambos:</span><span class="sxs-lookup"><span data-stu-id="f2aa3-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="f2aa3-111">modelos altamente mosaico e vs \_ 1 \_</span><span class="sxs-lookup"><span data-stu-id="f2aa3-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="f2aa3-112">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f2aa3-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="f2aa3-113">Iluminação difusa padrão versus PRT</span><span class="sxs-lookup"><span data-stu-id="f2aa3-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="f2aa3-114">A ilustração a seguir é renderizada usando o modelo de iluminação tradicional (n · l).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="f2aa3-115">As sombras nítidas poderiam ser habilitadas usando outra passagem e alguma forma de técnica de sombreamento (mapas de profundidade de sombra ou volumes de sombra).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="f2aa3-116">A adição de várias luzes exigiria várias passagens (se as sombras fossem usadas) ou sombreadores mais complexos com técnicas tradicionais.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![captura de tela de uma ilustração renderizada usando o modelo de iluminação tradicional](images/prt-diffuse-cropped.png)

<span data-ttu-id="f2aa3-118">A próxima ilustração é renderizada com PRT usando a melhor aproximação de uma única luz direcional que ele pode resolver.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="f2aa3-119">Isso resulta em sombras suaves que seriam difíceis de produzir com técnicas tradicionais.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="f2aa3-120">Como o PRT sempre modela os ambientes completos de iluminação adicionando várias luzes ou usando um mapa de ambiente, você só alteraria os valores (mas não o número) de constantes usadas pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![captura de tela de uma ilustração renderizada usando PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="f2aa3-122">PRT com interflexões</span><span class="sxs-lookup"><span data-stu-id="f2aa3-122">PRT with Interreflections</span></span>

<span data-ttu-id="f2aa3-123">A iluminação direta atinge a superfície diretamente da luz.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="f2aa3-124">As interflexões estão se esgotando na superfície após o encerramento de alguma outra superfície, certo número de vezes.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="f2aa3-125">O PRT pode modelar esse comportamento sem alterar o desempenho em tempo de execução simplesmente executando o simulador com parâmetros diferentes.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="f2aa3-126">A ilustração a seguir é criada usando somente o PRT direto (0 salta sem interflexões).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![captura de tela de uma ilustração renderizada usando somente o PRT direto](images/prt-nointerreflections.png)

<span data-ttu-id="f2aa3-128">A ilustração a seguir é criada usando o PRT com interflexões (2 salta com interflexões).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![captura de tela de uma ilustração renderizada usando o PRT com interflexões](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="f2aa3-130">PRT com dispersão de subsuperfície</span><span class="sxs-lookup"><span data-stu-id="f2aa3-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="f2aa3-131">A dispersão de subsuperfície é uma técnica que modela como a luz passa por determinados materiais.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="f2aa3-132">Por exemplo, pressione uma lanterna acesa em relação ao Palm de sua mão.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="f2aa3-133">A luz da lanterna passa por sua mão, salta (alterando a cor do processo) e sai do outro lado de sua mão.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="f2aa3-134">Isso também pode ser modelado com alterações simples no simulador e nenhuma alteração no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="f2aa3-135">A ilustração a seguir demonstra o PRT com dispersão de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![captura de tela de uma ilustração renderizada usando o PRT com dispersão de subsuperfície](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="f2aa3-137">Como o PRT funciona</span><span class="sxs-lookup"><span data-stu-id="f2aa3-137">How PRT Works</span></span>

<span data-ttu-id="f2aa3-138">Os termos a seguir são úteis para entender como o PRT funciona, conforme ilustrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="f2aa3-139">Radiante de origem: o radiante de origem representa o ambiente de iluminação como um todo.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="f2aa3-140">No PRT, um ambiente arbitrário é aproximado usando a base harmônica esférica – essa iluminação é considerada distante em relação ao objeto (a mesma suposição feita com mapas de ambiente).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="f2aa3-141">Saia de radiante: Exit radiante é a luz saindo de um ponto na superfície de qualquer fonte possível (refletida radiante, dispersão de subsuperfície, emissão).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="f2aa3-142">Vetores de transferência: os vetores de transferência mapeiam a origem radiante para Exit radiante e são preputados offline usando uma simulação de transporte leve complexa.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![diagrama de como o PRT funciona](images/prt-lightingpicture.png)

<span data-ttu-id="f2aa3-144">O PRT considera o processo de renderização em dois estágios, conforme mostrado no diagrama a seguir:</span><span class="sxs-lookup"><span data-stu-id="f2aa3-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="f2aa3-145">Uma simulação cara de transporte leve computa os coeficientes de transferência que podem ser usados em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="f2aa3-146">Um estágio de tempo de execução relativamente simples aproxima primeiro o ambiente de iluminação usando a base harmônica esférica, em seguida, usa esses coeficientes de iluminação e os coeficientes de transferência pré-computados (do estágio 1) com um sombreador simples, resultando na saída de radiante (a luz deixando o objeto).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![diagrama de fluxo de dados de PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="f2aa3-148">Como usar a API PRT</span><span class="sxs-lookup"><span data-stu-id="f2aa3-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="f2aa3-149">Compute os vetores de transferência com um dos cálculos... métodos de [**ID3DXPRTEngine**](id3dxprtengine.md).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="f2aa3-150">Lidar diretamente com esses vetores de transferência requer uma quantidade significativa de memória e computação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="f2aa3-151">A compactação reduz significativamente a quantidade de memória e a computação do sombreador necessários.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="f2aa3-152">Os valores de iluminação final são calculados em um sombreador de vértice que implementa a seguinte equação de renderização compactada.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![equação de renderização de PRT](images/prt-shaderequation.png)

    <span data-ttu-id="f2aa3-154">Em que:</span><span class="sxs-lookup"><span data-stu-id="f2aa3-154">Where:</span></span>

    

    | <span data-ttu-id="f2aa3-155">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2aa3-155">Parameter</span></span>      | <span data-ttu-id="f2aa3-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2aa3-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f2aa3-157">RP</span><span class="sxs-lookup"><span data-stu-id="f2aa3-157">Rₚ</span></span>             | <span data-ttu-id="f2aa3-158">Um único canal de saída radiante no vértice p e é avaliado em cada vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="f2aa3-159">MK</span><span class="sxs-lookup"><span data-stu-id="f2aa3-159">Mₖ</span></span>             | <span data-ttu-id="f2aa3-160">A média do cluster k.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-160">The mean for cluster k.</span></span> <span data-ttu-id="f2aa3-161">Este é um vetor de ordem ² de coeficientes.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="f2aa3-162">k</span><span class="sxs-lookup"><span data-stu-id="f2aa3-162">k</span></span>              | <span data-ttu-id="f2aa3-163">A ID do cluster para o vértice p.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="f2aa3-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="f2aa3-164">L<sup>'</sup></span></span>  | <span data-ttu-id="f2aa3-165">A aproximação do radiante de origem nas funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="f2aa3-166">Este é um vetor de ordem ² de coeficientes.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="f2aa3-167">j</span><span class="sxs-lookup"><span data-stu-id="f2aa3-167">j</span></span>              | <span data-ttu-id="f2aa3-168">Um inteiro que soma o número de vetores do PCA.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="f2aa3-169">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="f2aa3-169">w<sub>pj</sub></span></span> | <span data-ttu-id="f2aa3-170">O peso do PCA jth para o ponto p.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="f2aa3-171">Esse é um único coeficiente.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="f2aa3-172">B<sub>KJ</sub></span><span class="sxs-lookup"><span data-stu-id="f2aa3-172">B<sub>kj</sub></span></span> | <span data-ttu-id="f2aa3-173">O vetor de base do PCA do jth para o cluster k.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="f2aa3-174">Este é um vetor de ordem ² de coeficientes.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="f2aa3-175">A extração... os métodos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) fornecem acesso a dados compactados da simulação.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="f2aa3-176">Compute a origem radiante.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-176">Compute the source radiance.</span></span>

    <span data-ttu-id="f2aa3-177">Há várias funções auxiliares na API para lidar com uma variedade de cenários de iluminação comuns.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="f2aa3-178">Função</span><span class="sxs-lookup"><span data-stu-id="f2aa3-178">Function</span></span>                                                         | <span data-ttu-id="f2aa3-179">Finalidade</span><span class="sxs-lookup"><span data-stu-id="f2aa3-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="f2aa3-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="f2aa3-181">Aproxima uma luz direcional convencional.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="f2aa3-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="f2aa3-183">Aproxima fontes de luz esférica local.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="f2aa3-184">(Observe que o PRT só funciona com ambientes de iluminação de distância.)</span><span class="sxs-lookup"><span data-stu-id="f2aa3-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="f2aa3-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="f2aa3-186">Aproxima uma fonte de luz de área distante.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-186">Approximates a distant area light source.</span></span> <span data-ttu-id="f2aa3-187">Um exemplo seria o sol (ângulo de cone muito pequeno).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="f2aa3-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="f2aa3-189">Avalia uma luz que é uma interpolação linear entre duas cores (uma em cada pólo de uma esfera).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="f2aa3-190">Compute o radiante de saída.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="f2aa3-191">A equação 1 agora precisa ser avaliada em todos os pontos usando um vértice ou um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="f2aa3-192">Antes que o sombreador possa ser avaliado, as constantes devem ser computadas e carregadas na tabela de constantes (consulte a [amostra de demonstração de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="f2aa3-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="f2aa3-193">O próprio sombreador é uma implementação simples desta equação.</span><span class="sxs-lookup"><span data-stu-id="f2aa3-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="f2aa3-194">Referências</span><span class="sxs-lookup"><span data-stu-id="f2aa3-194">References</span></span>

<span data-ttu-id="f2aa3-195">Para obter mais informações sobre PRT e harmônicas esféricos, consulte os seguintes documentos:</span><span class="sxs-lookup"><span data-stu-id="f2aa3-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="f2aa3-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2aa3-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2aa3-197">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="f2aa3-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-198">Equações de PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f2aa3-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-199">Representando o PRT com texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f2aa3-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="f2aa3-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-204">Funções de transferência radiante preputadas</span><span class="sxs-lookup"><span data-stu-id="f2aa3-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="f2aa3-205">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f2aa3-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



