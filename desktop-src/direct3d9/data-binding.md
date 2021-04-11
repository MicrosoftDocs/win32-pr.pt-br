---
description: Use a coleção SasHostParameterValue para definir a coleção de valores do aplicativo host, bem como seu tipo e membros, expostos a efeitos.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Associação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104295957"
---
# <a name="data-binding"></a><span data-ttu-id="71aab-103">Associação de dados</span><span class="sxs-lookup"><span data-stu-id="71aab-103">Data Binding</span></span>

<span data-ttu-id="71aab-104">Use a [coleção SasHostParameterValue](#sashostparametervalue-collection) para definir a coleção de valores do aplicativo host, bem como seu tipo e membros, expostos a efeitos.</span><span class="sxs-lookup"><span data-stu-id="71aab-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="71aab-105">Use a anotação [SasBindAddress](#sasbindaddress) em um arquivo de efeito para associar um parâmetro de efeito ao seu parâmetro correspondente no aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="71aab-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="71aab-106">Coleção SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="71aab-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="71aab-107">O SasHostParameterValue é definido usando a sintaxe de arquivo de efeito (. FX).</span><span class="sxs-lookup"><span data-stu-id="71aab-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="71aab-108">Embora a sintaxe seja muito semelhante à sintaxe do arquivo de efeito, existem algumas diferenças.</span><span class="sxs-lookup"><span data-stu-id="71aab-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="71aab-109">Por exemplo, tipos de objeto, como Texture2D, amostras e cadeias de caracteres, não são válidos em arquivos de efeito reais, mas são válidos no SasHostParameterValue.</span><span class="sxs-lookup"><span data-stu-id="71aab-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="71aab-110">Um aplicativo host pode implementar o SasHostParameterValue de qualquer forma, desde que esteja de acordo com a descrição abaixo; a definição real está localizada no arquivo de inclusão do efeito padrão DXSAS ( \[ /Utilities/Source/SAS/SAS.fxh raiz do SDK \] ).</span><span class="sxs-lookup"><span data-stu-id="71aab-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="71aab-111">Observe que as matrizes no SasHostParameterValue, como luzes ou câmeras, têm comprimento não associado.</span><span class="sxs-lookup"><span data-stu-id="71aab-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="71aab-112">Isso significa que os efeitos podem ser associados a qualquer índice arbitrário nessas matrizes e os aplicativos de host devem fornecer padrões significativos nos casos em que nenhum valor de aplicativo pode ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="71aab-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="71aab-113">Alguns tipos e constantes são necessários para serem definidos no DXSAS padrão include, conforme observado na definição da inclusão padrão.</span><span class="sxs-lookup"><span data-stu-id="71aab-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="71aab-114">Isso permite que os efeitos associem facilmente os valores agregados do SasHostParameterValue aos parâmetros de efeito estruturados.</span><span class="sxs-lookup"><span data-stu-id="71aab-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="71aab-115">Coleção SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="71aab-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="71aab-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="71aab-116">Type</span></span>            | <span data-ttu-id="71aab-117">Membro</span><span class="sxs-lookup"><span data-stu-id="71aab-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="71aab-118">Hora</span><span class="sxs-lookup"><span data-stu-id="71aab-118">Time</span></span>](#time)                       | <span data-ttu-id="71aab-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="71aab-119">float</span></span>           | <span data-ttu-id="71aab-120">SAS. time. Now</span><span class="sxs-lookup"><span data-stu-id="71aab-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="71aab-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="71aab-121">float</span></span>           | <span data-ttu-id="71aab-122">SAS. time. Last</span><span class="sxs-lookup"><span data-stu-id="71aab-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="71aab-123">INT</span><span class="sxs-lookup"><span data-stu-id="71aab-123">int</span></span>             | <span data-ttu-id="71aab-124">SAS. time. FrameNumber</span><span class="sxs-lookup"><span data-stu-id="71aab-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="71aab-125">Mapa de ambiente</span><span class="sxs-lookup"><span data-stu-id="71aab-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="71aab-126">textureCUBE</span><span class="sxs-lookup"><span data-stu-id="71aab-126">textureCUBE</span></span>     | <span data-ttu-id="71aab-127">SAS. EnvironmentMap</span><span class="sxs-lookup"><span data-stu-id="71aab-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="71aab-128">Câmera</span><span class="sxs-lookup"><span data-stu-id="71aab-128">Camera</span></span>](#camera)                   | <span data-ttu-id="71aab-129">SasCamera</span><span class="sxs-lookup"><span data-stu-id="71aab-129">SasCamera</span></span>       | <span data-ttu-id="71aab-130">SAS. Camera</span><span class="sxs-lookup"><span data-stu-id="71aab-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="71aab-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="71aab-131">float4x4</span></span>        | <span data-ttu-id="71aab-132">SAS. Camera. WorldToView</span><span class="sxs-lookup"><span data-stu-id="71aab-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="71aab-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="71aab-133">float4x4</span></span>        | <span data-ttu-id="71aab-134">SAS. Camera. projeção</span><span class="sxs-lookup"><span data-stu-id="71aab-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="71aab-135">float2</span><span class="sxs-lookup"><span data-stu-id="71aab-135">float2</span></span>          | <span data-ttu-id="71aab-136">SAS. Camera. NearFarClipping</span><span class="sxs-lookup"><span data-stu-id="71aab-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="71aab-137">Claro</span><span class="sxs-lookup"><span data-stu-id="71aab-137">Light</span></span>](#light)                     | <span data-ttu-id="71aab-138">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="71aab-138">SasAmbientLight</span></span> | <span data-ttu-id="71aab-139">AmbientLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="71aab-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="71aab-140">INT</span><span class="sxs-lookup"><span data-stu-id="71aab-140">int</span></span>             | <span data-ttu-id="71aab-141">SAS. NumAmbientLights</span><span class="sxs-lookup"><span data-stu-id="71aab-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="71aab-142">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="71aab-142">SasAmbientLight</span></span> | <span data-ttu-id="71aab-143">DirectionalLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="71aab-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="71aab-144">INT</span><span class="sxs-lookup"><span data-stu-id="71aab-144">int</span></span>             | <span data-ttu-id="71aab-145">SAS. NumDirectionalLights</span><span class="sxs-lookup"><span data-stu-id="71aab-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="71aab-146">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="71aab-146">SasAmbientLight</span></span> | <span data-ttu-id="71aab-147">PointLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="71aab-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="71aab-148">INT</span><span class="sxs-lookup"><span data-stu-id="71aab-148">int</span></span>             | <span data-ttu-id="71aab-149">SAS. NumPointLights</span><span class="sxs-lookup"><span data-stu-id="71aab-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="71aab-150">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="71aab-150">SasAmbientLight</span></span> | <span data-ttu-id="71aab-151">\[ZeroOrMore Spotlight \] ;</span><span class="sxs-lookup"><span data-stu-id="71aab-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="71aab-152">INT</span><span class="sxs-lookup"><span data-stu-id="71aab-152">int</span></span>             | <span data-ttu-id="71aab-153">SAS. NumSpotLights</span><span class="sxs-lookup"><span data-stu-id="71aab-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="71aab-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="71aab-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="71aab-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="71aab-155">float4x4</span></span>        | <span data-ttu-id="71aab-156">SAS. Shadow \[ ZeroOrMore \] . WorldToShadow</span><span class="sxs-lookup"><span data-stu-id="71aab-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="71aab-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="71aab-157">texture2D</span></span>       | <span data-ttu-id="71aab-158">SAS. Shadow \[ ZeroOrMore \] . ShadowMap</span><span class="sxs-lookup"><span data-stu-id="71aab-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="71aab-159">Reduzida</span><span class="sxs-lookup"><span data-stu-id="71aab-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="71aab-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="71aab-160">float4x4</span></span>        | <span data-ttu-id="71aab-161">SAS. esqueleto. MeshToJointToWorld \[ OneOrMore\]</span><span class="sxs-lookup"><span data-stu-id="71aab-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="71aab-162">INT</span><span class="sxs-lookup"><span data-stu-id="71aab-162">int</span></span>             | <span data-ttu-id="71aab-163">SAS. esqueleto. NumJoints</span><span class="sxs-lookup"><span data-stu-id="71aab-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="71aab-164">Hora</span><span class="sxs-lookup"><span data-stu-id="71aab-164">Time</span></span>

<span data-ttu-id="71aab-165">O valor do relógio ou tempo virtual do aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="71aab-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="71aab-166">Os membros incluem:</span><span class="sxs-lookup"><span data-stu-id="71aab-166">Members include:</span></span>

-   <span data-ttu-id="71aab-167">SAS. time. Now-o valor do relógio virtual do aplicativo host no ponto em que o efeito será renderizado.</span><span class="sxs-lookup"><span data-stu-id="71aab-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="71aab-168">SAS. time. Last-o valor de agora na renderização anterior.</span><span class="sxs-lookup"><span data-stu-id="71aab-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="71aab-169">SAS. time. FrameNumber-o valor do contador que é incrementado uma vez por quadro renderizado.</span><span class="sxs-lookup"><span data-stu-id="71aab-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="71aab-170">Os efeitos devem lidar corretamente com o fato de que os valores desses membros podem ser encapsulados potencialmente durante tempos de execução extremamente longos.</span><span class="sxs-lookup"><span data-stu-id="71aab-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="71aab-171">Agora e o último podem ter valores muito grandes.</span><span class="sxs-lookup"><span data-stu-id="71aab-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="71aab-172">Mapa de ambiente</span><span class="sxs-lookup"><span data-stu-id="71aab-172">Environment Map</span></span>

<span data-ttu-id="71aab-173">Um mapa de ambiente cúbico.</span><span class="sxs-lookup"><span data-stu-id="71aab-173">A cubic environment map.</span></span> <span data-ttu-id="71aab-174">Os aplicativos host devem fornecer uma textura de cubo válida se um efeito tentar se associar a SAS. EnvironmentMap.</span><span class="sxs-lookup"><span data-stu-id="71aab-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="71aab-175">Câmera</span><span class="sxs-lookup"><span data-stu-id="71aab-175">Camera</span></span>

<span data-ttu-id="71aab-176">A câmera que está sendo renderizada no momento.</span><span class="sxs-lookup"><span data-stu-id="71aab-176">The camera currently being rendered.</span></span> <span data-ttu-id="71aab-177">Os membros incluem:</span><span class="sxs-lookup"><span data-stu-id="71aab-177">Members include:</span></span>

-   <span data-ttu-id="71aab-178">SAS. Camera. WorldToView-a matriz de exibição do mundo composto da câmera.</span><span class="sxs-lookup"><span data-stu-id="71aab-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="71aab-179">SAS. Camera. Projetion-a matriz de projeção da câmera.</span><span class="sxs-lookup"><span data-stu-id="71aab-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="71aab-180">SAS. Camera. NearFarClipping-os valores dos planos de recorte próximo e longe.</span><span class="sxs-lookup"><span data-stu-id="71aab-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="71aab-181">Claro</span><span class="sxs-lookup"><span data-stu-id="71aab-181">Light</span></span>

<span data-ttu-id="71aab-182">Uma ou mais luzes de cena.</span><span class="sxs-lookup"><span data-stu-id="71aab-182">One or more scene lights.</span></span> <span data-ttu-id="71aab-183">A coleção de luzes é declarada como uma matriz em que:</span><span class="sxs-lookup"><span data-stu-id="71aab-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="71aab-184">Cor-uma cor RGB.</span><span class="sxs-lookup"><span data-stu-id="71aab-184">Color - an RGB color.</span></span> <span data-ttu-id="71aab-185">O valor padrão é (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="71aab-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="71aab-186">Direção-a direção da luz.</span><span class="sxs-lookup"><span data-stu-id="71aab-186">Direction - the light direction.</span></span> <span data-ttu-id="71aab-187">O valor padrão é (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="71aab-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="71aab-188">Intervalo – a distância da luz em que os raios claros não têm efeito sobre a cena.</span><span class="sxs-lookup"><span data-stu-id="71aab-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="71aab-189">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="71aab-189">The default value is 0.</span></span>
-   <span data-ttu-id="71aab-190">Teta-o ângulo de cone interno de um Spotlight, medido em radianos.</span><span class="sxs-lookup"><span data-stu-id="71aab-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="71aab-191">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="71aab-191">The default value is 0.</span></span>
-   <span data-ttu-id="71aab-192">Phi-o ângulo de cone externo de um Spotlight, medido em radianos.</span><span class="sxs-lookup"><span data-stu-id="71aab-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="71aab-193">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="71aab-193">The default value is 0.</span></span>

<span data-ttu-id="71aab-194">O número de luzes deve ser definido como o número de luzes associadas à matriz associada.</span><span class="sxs-lookup"><span data-stu-id="71aab-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="71aab-195">Os efeitos podem optar por ignorar o número de luzes e associar a qualquer elemento de uma das matrizes leves.</span><span class="sxs-lookup"><span data-stu-id="71aab-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="71aab-196">Portanto, os aplicativos host devem fornecer uma Associação válida para elementos além do número de luzes na matriz.</span><span class="sxs-lookup"><span data-stu-id="71aab-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="71aab-197">ZeroOrMore implica que a matriz pode ter qualquer número de elementos.</span><span class="sxs-lookup"><span data-stu-id="71aab-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="71aab-198">Shadow</span><span class="sxs-lookup"><span data-stu-id="71aab-198">Shadow</span></span>

<span data-ttu-id="71aab-199">Buffers de sombra que consistem em:</span><span class="sxs-lookup"><span data-stu-id="71aab-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="71aab-200">WorldToShadow – uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="71aab-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="71aab-201">ShadowMap-um arquivo de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="71aab-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="71aab-202">ZeroOrMore implica que a matriz pode ter qualquer número de elementos (zero significa uma matriz vazia).</span><span class="sxs-lookup"><span data-stu-id="71aab-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="71aab-203">Um efeito declararia um amostra da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="71aab-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="71aab-204">Reduzida</span><span class="sxs-lookup"><span data-stu-id="71aab-204">Skeleton</span></span>

<span data-ttu-id="71aab-205">O conjunto de quadros que compõem o objeto de processamento no momento.</span><span class="sxs-lookup"><span data-stu-id="71aab-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="71aab-206">Os exemplos de quadro são Bones e transformações.</span><span class="sxs-lookup"><span data-stu-id="71aab-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="71aab-207">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="71aab-207">This includes:</span></span>

-   <span data-ttu-id="71aab-208">MeshToJointToWorld – uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="71aab-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="71aab-209">NumJoints-o número de junções no esqueleto.</span><span class="sxs-lookup"><span data-stu-id="71aab-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="71aab-210">OneOrMore implica que a matriz tem pelo menos uma e pode conter qualquer número de elementos.</span><span class="sxs-lookup"><span data-stu-id="71aab-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="71aab-211">A definição dá suporte a objetos de malha rígidas e com revestimento, usando o mesmo conjunto de valores de [coleção SasHostParameterValue](#sashostparametervalue-collection) com diferentes interpretações.</span><span class="sxs-lookup"><span data-stu-id="71aab-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="71aab-212">SasBindAddress</span><span class="sxs-lookup"><span data-stu-id="71aab-212">SasBindAddress</span></span>

<span data-ttu-id="71aab-213">Essa anotação é adicionada à parte superior de um arquivo de efeito para associar um parâmetro de efeito ao seu parâmetro correspondente definido na [coleção SasHostParameterValue](#sashostparametervalue-collection).</span><span class="sxs-lookup"><span data-stu-id="71aab-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="71aab-214">A anotação é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="71aab-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="71aab-215">Este exemplo associa a matriz mundial de efeito à matriz MeshToJointToWorld:</span><span class="sxs-lookup"><span data-stu-id="71aab-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="71aab-216">Essa anotação informa ao aplicativo host que ele precisa para definir o valor da matriz mundial de efeito usando os dados na matriz MeshToJointToWorld.</span><span class="sxs-lookup"><span data-stu-id="71aab-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="71aab-217">A sintaxe de anotação de endereço de associação foi definida para ser muito semelhante à sintaxe usada pelo [**ID3DXEffect**](id3dxeffect.md) para obter e definir parâmetros de efeito.</span><span class="sxs-lookup"><span data-stu-id="71aab-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="71aab-218">A única diferença entre os métodos DXSAS Grammar e **ID3DXEffect** é a adição do token de índice de asterisco.</span><span class="sxs-lookup"><span data-stu-id="71aab-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="71aab-219">Aqui está outro exemplo usando o índice de asterisco:</span><span class="sxs-lookup"><span data-stu-id="71aab-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="71aab-220">O token de índice de asterisco denota que todos os elementos da matriz de valores de envirnmant do host específico (cor, nesse caso) devem estar associados ao parâmetro associado.</span><span class="sxs-lookup"><span data-stu-id="71aab-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="71aab-221">Vários tokens de índice de asterisco permitem que os efeitos sejam associados a subelementos de uma matriz de estruturas sem a necessidade de associar toda a estrutura em si.</span><span class="sxs-lookup"><span data-stu-id="71aab-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="71aab-222">Este exemplo associa os valores de cor das seis primeiras luzes a um parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="71aab-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71aab-223">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71aab-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71aab-224">Referência de semântica e anotações padrão do DirectX</span><span class="sxs-lookup"><span data-stu-id="71aab-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



