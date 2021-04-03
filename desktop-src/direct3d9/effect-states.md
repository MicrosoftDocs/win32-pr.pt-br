---
description: Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674e72d818cd280bfe75a2cb02733576bc68319e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104010000"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="994ea-103">Estados de efeito (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="994ea-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="994ea-104">Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.</span><span class="sxs-lookup"><span data-stu-id="994ea-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="994ea-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="994ea-105">Where:</span></span>

-   <span data-ttu-id="994ea-106">Estado de efeito – semelhante aos Estados de pipeline de função fixa tradicional.</span><span class="sxs-lookup"><span data-stu-id="994ea-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="994ea-107">Uma lista completa de Estados é fornecida abaixo.</span><span class="sxs-lookup"><span data-stu-id="994ea-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="994ea-108">\[\[ \] índice \] do -Índice inteiro opcional.</span><span class="sxs-lookup"><span data-stu-id="994ea-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="994ea-109">O índice identifica um estado específico dentro de uma matriz de Estados de efeito.</span><span class="sxs-lookup"><span data-stu-id="994ea-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="994ea-110">Os colchetes externos indicam que um índice é opcional.</span><span class="sxs-lookup"><span data-stu-id="994ea-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="994ea-111">Se um índice for usado, certifique-se de usar os colchetes internos.</span><span class="sxs-lookup"><span data-stu-id="994ea-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="994ea-112">Expression – expressão de atribuição de estado.</span><span class="sxs-lookup"><span data-stu-id="994ea-112">expression - State assignment expression.</span></span> <span data-ttu-id="994ea-113">Consulte [Expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="994ea-114">Cada Estado tem um tipo de dados nativo.</span><span class="sxs-lookup"><span data-stu-id="994ea-114">Each state has a native data type.</span></span> <span data-ttu-id="994ea-115">Esse é o tipo de dados em que o estado espera que os valores estejam quando o efeito os atribui.</span><span class="sxs-lookup"><span data-stu-id="994ea-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="994ea-116">Os tipos de dados esperados por cada Estado estão listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="994ea-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="994ea-117">Observe que a interface de efeito tentará converter valores para o tipo apropriado o mais cedo possível.</span><span class="sxs-lookup"><span data-stu-id="994ea-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="994ea-118">Valores literais podem ser convertidos em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="994ea-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="994ea-119">Não literais (ou seja, variáveis regulares) precisam ser convertidas quando os métodos definidos apropriados são chamados.</span><span class="sxs-lookup"><span data-stu-id="994ea-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="994ea-120">Por exemplo, a interface de efeito converterá valores definidos usando [**setbool**](id3dxbaseeffect--setbool.md), [**DefinirValor**](id3dxbaseeffect--setvalue.md)e outras funções semelhantes, se necessário.</span><span class="sxs-lookup"><span data-stu-id="994ea-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="994ea-121">Para melhorar o desempenho, verifique se os valores passados para a interface de efeito já são do tipo correto e não precisarão de conversão.</span><span class="sxs-lookup"><span data-stu-id="994ea-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="994ea-122">Se o tempo de execução não puder converter um valor, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="994ea-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="994ea-123">Os Estados de efeito podem ser divididos nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="994ea-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="994ea-124">Estados claros</span><span class="sxs-lookup"><span data-stu-id="994ea-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="994ea-125">Estados de material</span><span class="sxs-lookup"><span data-stu-id="994ea-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="994ea-126">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="994ea-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="994ea-127">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="994ea-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="994ea-128">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="994ea-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="994ea-129">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="994ea-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="994ea-130">Estados de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="994ea-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="994ea-131">Estados do sombreador</span><span class="sxs-lookup"><span data-stu-id="994ea-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="994ea-132">Estados de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="994ea-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="994ea-133">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="994ea-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="994ea-134">Estados de estágio de textura</span><span class="sxs-lookup"><span data-stu-id="994ea-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="994ea-135">Estados de transformação</span><span class="sxs-lookup"><span data-stu-id="994ea-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="994ea-136">Estados claros</span><span class="sxs-lookup"><span data-stu-id="994ea-136">Light States</span></span>

<span data-ttu-id="994ea-137">Para habilitar o melhor desempenho para a aplicação de um efeito, todos os componentes de uma luz ou um material devem ser especificados no arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="994ea-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="994ea-138">Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de luz individualmente.</span><span class="sxs-lookup"><span data-stu-id="994ea-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994ea-139">Estado claro</span><span class="sxs-lookup"><span data-stu-id="994ea-139">Light State</span></span>            | <span data-ttu-id="994ea-140">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-140">Type</span></span>   | <span data-ttu-id="994ea-141">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="994ea-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="994ea-143">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-143">float4</span></span> | <span data-ttu-id="994ea-144">Consulte o membro de ambiente de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="994ea-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="994ea-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-146">float</span></span>  | <span data-ttu-id="994ea-147">Consulte o membro Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="994ea-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="994ea-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-149">float</span></span>  | <span data-ttu-id="994ea-150">Consulte o membro Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="994ea-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="994ea-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-152">float</span></span>  | <span data-ttu-id="994ea-153">Consulte o membro Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="994ea-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="994ea-155">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-155">float4</span></span> | <span data-ttu-id="994ea-156">Consulte o membro difuso de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="994ea-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="994ea-158">float3</span><span class="sxs-lookup"><span data-stu-id="994ea-158">float3</span></span> | <span data-ttu-id="994ea-159">Consulte o membro de direção de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="994ea-160">N mais claro \[\]</span><span class="sxs-lookup"><span data-stu-id="994ea-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="994ea-161">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-161">bool</span></span>   | <span data-ttu-id="994ea-162">**True** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="994ea-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="994ea-163">Consulte o argumento bEnable em [**clarear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="994ea-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="994ea-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="994ea-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-165">float</span></span>  | <span data-ttu-id="994ea-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="994ea-167">Consulte o membro de queda de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="994ea-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="994ea-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-169">float</span></span>  | <span data-ttu-id="994ea-170">Consulte o membro Phi de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="994ea-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="994ea-172">float3</span><span class="sxs-lookup"><span data-stu-id="994ea-172">float3</span></span> | <span data-ttu-id="994ea-173">Consulte o membro position de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="994ea-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-174">LightRange\[n\]</span></span>        | <span data-ttu-id="994ea-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-175">float</span></span>  | <span data-ttu-id="994ea-176">Consulte o membro Range de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="994ea-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="994ea-178">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-178">float4</span></span> | <span data-ttu-id="994ea-179">Consulte o membro especular de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="994ea-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="994ea-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-181">float</span></span>  | <span data-ttu-id="994ea-182">Consulte o membro teta de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="994ea-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="994ea-183">LightType\[n\]</span></span>         | <span data-ttu-id="994ea-184">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-184">dword</span></span>  | <span data-ttu-id="994ea-185">Mesmo valor que a matriz de até n valores de [**D3DLIGHTTYPE**](./d3dlighttype.md) sem o \_ prefixo D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="994ea-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="994ea-186">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="994ea-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="994ea-187">Isso habilitará a iluminação, tornará a iluminação do tipo, definirá a posição da luz como float3<10.0 f, 1,0 f, 23.0 f> e definirá a cor do ambiente como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1.0>.</span><span class="sxs-lookup"><span data-stu-id="994ea-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="994ea-188">Estados de material</span><span class="sxs-lookup"><span data-stu-id="994ea-188">Material States</span></span>

<span data-ttu-id="994ea-189">Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de material individualmente.</span><span class="sxs-lookup"><span data-stu-id="994ea-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="994ea-190">Estado do material</span><span class="sxs-lookup"><span data-stu-id="994ea-190">Material State</span></span>   | <span data-ttu-id="994ea-191">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-191">Type</span></span>   | <span data-ttu-id="994ea-192">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-192">Values</span></span>                                         |
| <span data-ttu-id="994ea-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="994ea-193">MaterialAmbient</span></span>  | <span data-ttu-id="994ea-194">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-194">float4</span></span> | <span data-ttu-id="994ea-195">Mesmo valor que o [ **ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="994ea-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="994ea-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="994ea-196">MaterialDiffuse</span></span>  | <span data-ttu-id="994ea-197">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-197">float4</span></span> | <span data-ttu-id="994ea-198">Mesmo valor que [ **difusa**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="994ea-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="994ea-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="994ea-199">MaterialEmissive</span></span> | <span data-ttu-id="994ea-200">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-200">float4</span></span> | <span data-ttu-id="994ea-201">Mesmo valor que [ **emissiva**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="994ea-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="994ea-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="994ea-202">MaterialPower</span></span>    | <span data-ttu-id="994ea-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-203">float</span></span>  | <span data-ttu-id="994ea-204">Mesmo valor que a [ **energia**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="994ea-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="994ea-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="994ea-205">MaterialSpecular</span></span> | <span data-ttu-id="994ea-206">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-206">float4</span></span> | <span data-ttu-id="994ea-207">Mesmo valor que [ **especular**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="994ea-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="994ea-208">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="994ea-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="994ea-209">Isso definirá a cor difusa como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f> e tornará o poder do material 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="994ea-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="994ea-210">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="994ea-210">Render States</span></span>

<span data-ttu-id="994ea-211">Há dois tipos de Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="994ea-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="994ea-212">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="994ea-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="994ea-213">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="994ea-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="994ea-214">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="994ea-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="994ea-215">Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="994ea-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="994ea-216">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="994ea-216">Render State</span></span></td>
<td><span data-ttu-id="994ea-217">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-217">Type</span></span></td>
<td><span data-ttu-id="994ea-218">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="994ea-220">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-220">bool</span></span></td>
<td><span data-ttu-id="994ea-221">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-221">True or False.</span></span> <span data-ttu-id="994ea-222">Os mesmos valores que D3DRS_ALPHABLENDENABLE em <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="994ea-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="994ea-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="994ea-224">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-224">dword</span></span></td>
<td><span data-ttu-id="994ea-225">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="994ea-226">Consulte D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="994ea-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="994ea-227">AlphaRef</span></span></td>
<td><span data-ttu-id="994ea-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-228">dword</span></span></td>
<td><span data-ttu-id="994ea-229">Mesmos valores que D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="994ea-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="994ea-231">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-231">dword</span></span></td>
<td><span data-ttu-id="994ea-232">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-232">True or False.</span></span> <span data-ttu-id="994ea-233">Consulte D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="994ea-234">BlendOp</span></span></td>
<td><span data-ttu-id="994ea-235">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-235">dword</span></span></td>
<td><span data-ttu-id="994ea-236">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sem o prefixo D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="994ea-238">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-238">dword</span></span></td>
<td><span data-ttu-id="994ea-239">Combinação de bits de vermelho | VERDE | AZUL | Alfa.</span><span class="sxs-lookup"><span data-stu-id="994ea-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="994ea-240">Consulte D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="994ea-241">DepthBias</span></span></td>
<td><span data-ttu-id="994ea-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-242">float</span></span></td>
<td><span data-ttu-id="994ea-243">Mesmos valores que D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="994ea-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="994ea-244">DestBlend</span></span></td>
<td><span data-ttu-id="994ea-245">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-245">dword</span></span></td>
<td><span data-ttu-id="994ea-246">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="994ea-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-247">DitherEnable</span></span></td>
<td><span data-ttu-id="994ea-248">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-248">bool</span></span></td>
<td><span data-ttu-id="994ea-249">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-249">True or False.</span></span> <span data-ttu-id="994ea-250">Mesmos valores que D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="994ea-251">FillMode</span></span></td>
<td><span data-ttu-id="994ea-252">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-252">dword</span></span></td>
<td><span data-ttu-id="994ea-253">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sem o prefixo D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="994ea-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="994ea-254">LastPixel</span></span></td>
<td><span data-ttu-id="994ea-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-255">dword</span></span></td>
<td><span data-ttu-id="994ea-256">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-256">True or False.</span></span> <span data-ttu-id="994ea-257">Consulte D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="994ea-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-258">Shadmode</span><span class="sxs-lookup"><span data-stu-id="994ea-258">ShadeMode</span></span></td>
<td><span data-ttu-id="994ea-259">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-259">dword</span></span></td>
<td><span data-ttu-id="994ea-260">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sem o prefixo D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="994ea-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="994ea-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="994ea-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-262">float</span></span></td>
<td><span data-ttu-id="994ea-263">Mesmos valores que D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="994ea-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="994ea-264">SrcBlend</span></span></td>
<td><span data-ttu-id="994ea-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-265">dword</span></span></td>
<td><span data-ttu-id="994ea-266">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="994ea-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-267">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-267">StencilEnable</span></span></td>
<td><span data-ttu-id="994ea-268">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-268">bool</span></span></td>
<td><span data-ttu-id="994ea-269">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-269">True or False.</span></span> <span data-ttu-id="994ea-270">Mesmos valores que D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-270">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-271">StencilFail</span><span class="sxs-lookup"><span data-stu-id="994ea-271">StencilFail</span></span></td>
<td><span data-ttu-id="994ea-272">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-272">dword</span></span></td>
<td><span data-ttu-id="994ea-273">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-273">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="994ea-274">Consulte D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="994ea-274">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-275">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="994ea-275">StencilFunc</span></span></td>
<td><span data-ttu-id="994ea-276">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-276">dword</span></span></td>
<td><span data-ttu-id="994ea-277">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-277">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="994ea-278">Consulte D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="994ea-278">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-279">StencilMask</span><span class="sxs-lookup"><span data-stu-id="994ea-279">StencilMask</span></span></td>
<td><span data-ttu-id="994ea-280">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-280">dword</span></span></td>
<td><span data-ttu-id="994ea-281">Mesmos valores que D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="994ea-281">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-282">StencilPass</span><span class="sxs-lookup"><span data-stu-id="994ea-282">StencilPass</span></span></td>
<td><span data-ttu-id="994ea-283">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-283">dword</span></span></td>
<td><span data-ttu-id="994ea-284">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-284">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="994ea-285">Consulte D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="994ea-285">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-286">StencilRef</span><span class="sxs-lookup"><span data-stu-id="994ea-286">StencilRef</span></span></td>
<td><span data-ttu-id="994ea-287">INT</span><span class="sxs-lookup"><span data-stu-id="994ea-287">int</span></span></td>
<td><span data-ttu-id="994ea-288">Mesmos valores que D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="994ea-288">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-289">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="994ea-289">StencilWriteMask</span></span></td>
<td><span data-ttu-id="994ea-290">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-290">dword</span></span></td>
<td><span data-ttu-id="994ea-291">Mesmos valores que D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="994ea-291">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-292">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="994ea-292">StencilZFail</span></span></td>
<td><span data-ttu-id="994ea-293">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-293">dword</span></span></td>
<td><span data-ttu-id="994ea-294">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-294">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="994ea-295">Consulte D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="994ea-295">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-296">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="994ea-296">TextureFactor</span></span></td>
<td><span data-ttu-id="994ea-297">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-297">dword</span></span></td>
<td><span data-ttu-id="994ea-298">Mesmos valores que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="994ea-298">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="994ea-299">Mesmos valores que D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="994ea-299">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-300">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="994ea-300">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="994ea-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-301">dword</span></span></td>
<td><span data-ttu-id="994ea-302">Os valores são os mesmos que os valores usados pelo D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="994ea-302">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="994ea-303">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="994ea-303">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="994ea-304">COORD0 (que corresponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="994ea-304">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="994ea-305">COORD1 (que corresponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="994ea-305">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="994ea-306">COORD2 (que corresponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="994ea-306">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="994ea-307">COORD3 (que corresponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="994ea-307">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="994ea-308">U (que corresponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="994ea-308">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="994ea-309">V (que corresponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="994ea-309">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="994ea-310">W (que corresponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="994ea-310">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-311">ZEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-311">ZEnable</span></span></td>
<td><span data-ttu-id="994ea-312">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-312">dword</span></span></td>
<td><span data-ttu-id="994ea-313">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sem o prefixo D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="994ea-313">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994ea-314">ZFunc</span><span class="sxs-lookup"><span data-stu-id="994ea-314">ZFunc</span></span></td>
<td><span data-ttu-id="994ea-315">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-315">dword</span></span></td>
<td><span data-ttu-id="994ea-316">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="994ea-316">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="994ea-317">Consulte D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="994ea-317">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994ea-318">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-318">ZWriteEnable</span></span></td>
<td><span data-ttu-id="994ea-319">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-319">bool</span></span></td>
<td><span data-ttu-id="994ea-320">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-320">True or False.</span></span> <span data-ttu-id="994ea-321">Consulte D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-321">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="994ea-322">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="994ea-322">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="994ea-323">Isso habilitará a mistura alfa e fará com que todas as geometrias sejam renderizadas em wireframe.</span><span class="sxs-lookup"><span data-stu-id="994ea-323">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="994ea-324">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="994ea-324">Vertex Pipe Render States</span></span>

<span data-ttu-id="994ea-325">Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="994ea-325">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994ea-326">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="994ea-326">Render State</span></span>             | <span data-ttu-id="994ea-327">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-327">Type</span></span>   | <span data-ttu-id="994ea-328">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-328">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="994ea-329">Ambiente</span><span class="sxs-lookup"><span data-stu-id="994ea-329">Ambient</span></span>                  | <span data-ttu-id="994ea-330">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-330">float4</span></span> | <span data-ttu-id="994ea-331">Mesmos valores que D3DRS \_ ambiente.</span><span class="sxs-lookup"><span data-stu-id="994ea-331">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="994ea-332">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="994ea-332">AmbientMaterialSource</span></span>    | <span data-ttu-id="994ea-333">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-333">dword</span></span>  | <span data-ttu-id="994ea-334">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="994ea-334">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="994ea-335">Consulte D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="994ea-335">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="994ea-336">Recortando</span><span class="sxs-lookup"><span data-stu-id="994ea-336">Clipping</span></span>                 | <span data-ttu-id="994ea-337">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-337">bool</span></span>   | <span data-ttu-id="994ea-338">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-338">True or False.</span></span> <span data-ttu-id="994ea-339">Mesmos valores que o \_ recorte de D3DRS.</span><span class="sxs-lookup"><span data-stu-id="994ea-339">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="994ea-340">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-340">ClipPlaneEnable</span></span>          | <span data-ttu-id="994ea-341">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-341">dword</span></span>  | <span data-ttu-id="994ea-342">Combinação de bits de D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="994ea-342">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="994ea-343">Consulte [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-343">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="994ea-344">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="994ea-344">ColorVertex</span></span>              | <span data-ttu-id="994ea-345">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-345">bool</span></span>   | <span data-ttu-id="994ea-346">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-346">True or False.</span></span> <span data-ttu-id="994ea-347">Mesmos valores que D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="994ea-347">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="994ea-348">De seleção</span><span class="sxs-lookup"><span data-stu-id="994ea-348">CullMode</span></span>                 | <span data-ttu-id="994ea-349">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-349">dword</span></span>  | <span data-ttu-id="994ea-350">Mesmos valores que [**D3DCULL**](./d3dcull.md) sem o \_ prefixo D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="994ea-350">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="994ea-351">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="994ea-351">DiffuseMaterialSource</span></span>    | <span data-ttu-id="994ea-352">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-352">dword</span></span>  | <span data-ttu-id="994ea-353">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="994ea-353">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="994ea-354">Consulte D3DRS \_ DiffuseMaterialSource.</span><span class="sxs-lookup"><span data-stu-id="994ea-354">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="994ea-355">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="994ea-355">EmissiveMaterialSource</span></span>   | <span data-ttu-id="994ea-356">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-356">dword</span></span>  | <span data-ttu-id="994ea-357">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="994ea-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="994ea-358">Consulte D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="994ea-358">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="994ea-359">FogColor</span><span class="sxs-lookup"><span data-stu-id="994ea-359">FogColor</span></span>                 | <span data-ttu-id="994ea-360">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-360">dword</span></span>  | <span data-ttu-id="994ea-361">Mesmos valores que [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-361">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="994ea-362">Consulte D3DRS \_ FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="994ea-362">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="994ea-363">FogDensity</span><span class="sxs-lookup"><span data-stu-id="994ea-363">FogDensity</span></span>               | <span data-ttu-id="994ea-364">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-364">float</span></span>  | <span data-ttu-id="994ea-365">Mesmos valores que D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="994ea-365">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="994ea-366">FogEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-366">FogEnable</span></span>                | <span data-ttu-id="994ea-367">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-367">bool</span></span>   | <span data-ttu-id="994ea-368">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-368">True or False.</span></span> <span data-ttu-id="994ea-369">Mesmos valores que D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-369">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="994ea-370">FogEnd</span><span class="sxs-lookup"><span data-stu-id="994ea-370">FogEnd</span></span>                   | <span data-ttu-id="994ea-371">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-371">float</span></span>  | <span data-ttu-id="994ea-372">Mesmos valores que D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="994ea-372">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="994ea-373">FogStart</span><span class="sxs-lookup"><span data-stu-id="994ea-373">FogStart</span></span>                 | <span data-ttu-id="994ea-374">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-374">float</span></span>  | <span data-ttu-id="994ea-375">Mesmos valores que D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="994ea-375">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="994ea-376">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="994ea-376">FogTableMode</span></span>             | <span data-ttu-id="994ea-377">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-377">dword</span></span>  | <span data-ttu-id="994ea-378">Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-378">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="994ea-379">Consulte D3DRS \_ FOGTABLEMODE no [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="994ea-379">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="994ea-380">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="994ea-380">FogVertexMode</span></span>            | <span data-ttu-id="994ea-381">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-381">dword</span></span>  | <span data-ttu-id="994ea-382">Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md) sem o \_ prefixo D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="994ea-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="994ea-383">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-383">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="994ea-384">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-384">bool</span></span>   | <span data-ttu-id="994ea-385">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-385">True or False.</span></span> <span data-ttu-id="994ea-386">Mesmos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-386">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="994ea-387">Iluminação</span><span class="sxs-lookup"><span data-stu-id="994ea-387">Lighting</span></span>                 | <span data-ttu-id="994ea-388">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-388">bool</span></span>   | <span data-ttu-id="994ea-389">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-389">True or False.</span></span> <span data-ttu-id="994ea-390">Mesmos valores que a \_ iluminação D3DRS.</span><span class="sxs-lookup"><span data-stu-id="994ea-390">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="994ea-391">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="994ea-391">LocalViewer</span></span>              | <span data-ttu-id="994ea-392">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-392">bool</span></span>   | <span data-ttu-id="994ea-393">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-393">True or False.</span></span> <span data-ttu-id="994ea-394">Mesmos valores que D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="994ea-394">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="994ea-395">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="994ea-395">MultiSampleAntialias</span></span>     | <span data-ttu-id="994ea-396">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-396">bool</span></span>   | <span data-ttu-id="994ea-397">Mesmos valores que D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="994ea-397">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="994ea-398">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="994ea-398">MultiSampleMask</span></span>          | <span data-ttu-id="994ea-399">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-399">dword</span></span>  | <span data-ttu-id="994ea-400">Mesmos valores que D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="994ea-400">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="994ea-401">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="994ea-401">NormalizeNormals</span></span>         | <span data-ttu-id="994ea-402">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-402">bool</span></span>   | <span data-ttu-id="994ea-403">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-403">True or False.</span></span> <span data-ttu-id="994ea-404">Mesmos valores que D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="994ea-404">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="994ea-405">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="994ea-405">PatchSegments</span></span>            | <span data-ttu-id="994ea-406">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-406">float</span></span>  | <span data-ttu-id="994ea-407">Mesmos valores que nSegments em [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="994ea-407">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="994ea-408">PointScale \_ A</span><span class="sxs-lookup"><span data-stu-id="994ea-408">PointScale\_A</span></span>            | <span data-ttu-id="994ea-409">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-409">float</span></span>  | <span data-ttu-id="994ea-410">Os mesmos valores que D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="994ea-410">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="994ea-411">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="994ea-411">PointScale\_B</span></span>            | <span data-ttu-id="994ea-412">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-412">float</span></span>  | <span data-ttu-id="994ea-413">Os mesmos valores que D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="994ea-413">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="994ea-414">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="994ea-414">PointScale\_C</span></span>            | <span data-ttu-id="994ea-415">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-415">float</span></span>  | <span data-ttu-id="994ea-416">Os mesmos valores que D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="994ea-416">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="994ea-417">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-417">PointScaleEnable</span></span>         | <span data-ttu-id="994ea-418">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-418">bool</span></span>   | <span data-ttu-id="994ea-419">Mesmos valores que D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-419">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="994ea-420">Pontos</span><span class="sxs-lookup"><span data-stu-id="994ea-420">PointSize</span></span>                | <span data-ttu-id="994ea-421">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-421">float</span></span>  | <span data-ttu-id="994ea-422">Os mesmos valores que D3DRS \_ apontam.</span><span class="sxs-lookup"><span data-stu-id="994ea-422">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="994ea-423">Pontos \_ mínimos</span><span class="sxs-lookup"><span data-stu-id="994ea-423">PointSize\_Min</span></span>           | <span data-ttu-id="994ea-424">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-424">float</span></span>  | <span data-ttu-id="994ea-425">Os mesmos valores que D3DRS \_ apontam \_ mín.</span><span class="sxs-lookup"><span data-stu-id="994ea-425">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="994ea-426">Pontos \_ máximos</span><span class="sxs-lookup"><span data-stu-id="994ea-426">PointSize\_Max</span></span>           | <span data-ttu-id="994ea-427">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-427">float</span></span>  | <span data-ttu-id="994ea-428">Os mesmos valores que D3DRS \_ aponta para \_ Max sem o \_ prefixo D3DRS.</span><span class="sxs-lookup"><span data-stu-id="994ea-428">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="994ea-429">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-429">PointSpriteEnable</span></span>        | <span data-ttu-id="994ea-430">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-430">bool</span></span>   | <span data-ttu-id="994ea-431">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-431">True or False.</span></span> <span data-ttu-id="994ea-432">Mesmos valores que D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-432">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="994ea-433">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-433">RangeFogEnable</span></span>           | <span data-ttu-id="994ea-434">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-434">bool</span></span>   | <span data-ttu-id="994ea-435">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-435">True or False.</span></span> <span data-ttu-id="994ea-436">Mesmos valores que D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-436">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="994ea-437">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="994ea-437">SpecularEnable</span></span>           | <span data-ttu-id="994ea-438">bool</span><span class="sxs-lookup"><span data-stu-id="994ea-438">bool</span></span>   | <span data-ttu-id="994ea-439">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="994ea-439">True or False.</span></span> <span data-ttu-id="994ea-440">Mesmos valores que D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="994ea-440">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="994ea-441">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="994ea-441">SpecularMaterialSource</span></span>   | <span data-ttu-id="994ea-442">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-442">dword</span></span>  | <span data-ttu-id="994ea-443">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="994ea-443">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="994ea-444">Consulte D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="994ea-444">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="994ea-445">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="994ea-445">TweenFactor</span></span>              | <span data-ttu-id="994ea-446">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-446">float</span></span>  | <span data-ttu-id="994ea-447">Mesmos valores que D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="994ea-447">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="994ea-448">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="994ea-448">VertexBlend</span></span>              | <span data-ttu-id="994ea-449">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-449">dword</span></span>  | <span data-ttu-id="994ea-450">Mesmos valores que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sem o \_ prefixo D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="994ea-450">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="994ea-451">Consulte D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="994ea-451">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="994ea-452">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="994ea-452">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="994ea-453">Isso fará com que a cor do ambiente FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f>, defina o modo de remoção do backface como contador no sentido anti-horário e defina a cor da neblina como vermelha.</span><span class="sxs-lookup"><span data-stu-id="994ea-453">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="994ea-454">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="994ea-454">Sampler States</span></span>

<span data-ttu-id="994ea-455">Um estado de amostra representa um objeto de amostra.</span><span class="sxs-lookup"><span data-stu-id="994ea-455">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="994ea-456">Estado</span><span class="sxs-lookup"><span data-stu-id="994ea-456">State</span></span>   | <span data-ttu-id="994ea-457">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-457">Type</span></span>    | <span data-ttu-id="994ea-458">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-458">Values</span></span>                              |
| <span data-ttu-id="994ea-459">Exemplo</span><span class="sxs-lookup"><span data-stu-id="994ea-459">Sampler</span></span> | <span data-ttu-id="994ea-460">cores</span><span class="sxs-lookup"><span data-stu-id="994ea-460">sampler</span></span> | <span data-ttu-id="994ea-461">**NULL** ou um bloco de estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="994ea-461">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="994ea-462">Estados de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="994ea-462">Sampler Stage States</span></span>

<span data-ttu-id="994ea-463">Os Estados de estágio de amostra são usados para amostras de texturas.</span><span class="sxs-lookup"><span data-stu-id="994ea-463">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="994ea-464">O estado de amostra determina os tipos de filtragem e os modos de endereçamento de textura.</span><span class="sxs-lookup"><span data-stu-id="994ea-464">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994ea-465">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="994ea-465">Sampler State</span></span>       | <span data-ttu-id="994ea-466">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-466">Type</span></span>                         | <span data-ttu-id="994ea-467">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-467">Values</span></span>                                                                                                                            |
| <span data-ttu-id="994ea-468">Endereço de \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-468">AddressU\[16\]</span></span>      | <span data-ttu-id="994ea-469">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-469">dword</span></span>                        | <span data-ttu-id="994ea-470">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="994ea-470">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="994ea-471">Consulte D3DSAMP \_ AddressU.</span><span class="sxs-lookup"><span data-stu-id="994ea-471">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="994ea-472">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-472">AddressV\[16\]</span></span>      | <span data-ttu-id="994ea-473">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-473">dword</span></span>                        | <span data-ttu-id="994ea-474">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="994ea-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="994ea-475">Consulte D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="994ea-475">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="994ea-476">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-476">AddressW\[16\]</span></span>      | <span data-ttu-id="994ea-477">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-477">dword</span></span>                        | <span data-ttu-id="994ea-478">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="994ea-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="994ea-479">Consulte D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="994ea-479">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="994ea-480">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-480">BorderColor\[16\]</span></span>   | [<span data-ttu-id="994ea-481">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="994ea-481">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="994ea-482">Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="994ea-482">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="994ea-483">Consulte D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="994ea-483">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="994ea-484">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-484">MagFilter\[16\]</span></span>     | <span data-ttu-id="994ea-485">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-485">dword</span></span>                        | <span data-ttu-id="994ea-486">Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="994ea-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="994ea-487">Consulte D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="994ea-487">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="994ea-488">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-488">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="994ea-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-489">dword</span></span>                        | <span data-ttu-id="994ea-490">Os mesmos valores que D3DSAMP \_ MAXANISOTROPY sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="994ea-490">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="994ea-491">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-491">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="994ea-492">INT</span><span class="sxs-lookup"><span data-stu-id="994ea-492">int</span></span>                          | <span data-ttu-id="994ea-493">Os mesmos valores que D3DSAMP \_ MAXMIPLEVEL sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="994ea-493">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="994ea-494">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-494">MinFilter\[16\]</span></span>     | <span data-ttu-id="994ea-495">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-495">dword</span></span>                        | <span data-ttu-id="994ea-496">Os mesmos valores que D3DSAMP \_ MINFILTER sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="994ea-496">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="994ea-497">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-497">MipFilter\[16\]</span></span>     | <span data-ttu-id="994ea-498">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-498">dword</span></span>                        | <span data-ttu-id="994ea-499">Os mesmos valores que D3DSAMP \_ MIPFILTER sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="994ea-499">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="994ea-500">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="994ea-500">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="994ea-501">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-501">float</span></span>                        | <span data-ttu-id="994ea-502">Os mesmos valores que D3DSAMP \_ MIPMAPLODBIAS sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="994ea-502">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="994ea-503">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="994ea-503">SRGBTexture</span></span>         | <span data-ttu-id="994ea-504">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-504">float</span></span>                        | <span data-ttu-id="994ea-505">Mesmo valor que D3DSAMP \_ SRGBTEXTURE sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="994ea-505">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                  |



 

<span data-ttu-id="994ea-506">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="994ea-506">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="994ea-507">Isso coloca UVW valores entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="994ea-507">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="994ea-508">Estados do sombreador</span><span class="sxs-lookup"><span data-stu-id="994ea-508">Shader States</span></span>

<span data-ttu-id="994ea-509">Há apenas dois Estados de sombreador de efeito: um associado a um objeto de sombreador de vértice e o outro associado a um objeto de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="994ea-509">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="994ea-510">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="994ea-510">Shader State</span></span> | <span data-ttu-id="994ea-511">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-511">Type</span></span>         | <span data-ttu-id="994ea-512">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-512">Values</span></span>                                                                      |
| <span data-ttu-id="994ea-513">PixelShader</span><span class="sxs-lookup"><span data-stu-id="994ea-513">PixelShader</span></span>  | <span data-ttu-id="994ea-514">PixelShader</span><span class="sxs-lookup"><span data-stu-id="994ea-514">pixelshader</span></span>  | <span data-ttu-id="994ea-515">**NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="994ea-515">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="994ea-516">VertexShader</span><span class="sxs-lookup"><span data-stu-id="994ea-516">VertexShader</span></span> | <span data-ttu-id="994ea-517">vertexshader</span><span class="sxs-lookup"><span data-stu-id="994ea-517">vertexshader</span></span> | <span data-ttu-id="994ea-518">**NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="994ea-518">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="994ea-519">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="994ea-519">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="994ea-520">Isso compilará VSTexture, um sombreador de vértice definido anteriormente no arquivo. FX, para o vertex shader versão 1,1 e, em seguida, definirá esse sombreador compilado como o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="994ea-520">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="994ea-521">O sombreador de pixel é atribuído a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="994ea-521">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="994ea-522">Estados de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="994ea-522">Shader Constant States</span></span>

<span data-ttu-id="994ea-523">Os Estados de constante do sombreador são usados para acessar parâmetros de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="994ea-523">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="994ea-524">Estado de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="994ea-524">Shader Constant State</span></span> | <span data-ttu-id="994ea-525">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-525">Type</span></span>            | <span data-ttu-id="994ea-526">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-526">Values</span></span>                                       |
| <span data-ttu-id="994ea-527">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="994ea-527">PixelShaderConstant</span></span>   | <span data-ttu-id="994ea-528">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-528">float\[m\[n\]\]</span></span> | <span data-ttu-id="994ea-529">matriz m x n de floats; m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-529">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="994ea-530">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="994ea-530">PixelShaderConstant1</span></span>  | <span data-ttu-id="994ea-531">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-531">float4</span></span>          | <span data-ttu-id="994ea-532">Um 4D flutuante.</span><span class="sxs-lookup"><span data-stu-id="994ea-532">One 4D float.</span></span>                                |
| <span data-ttu-id="994ea-533">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="994ea-533">PixelShaderConstant2</span></span>  | <span data-ttu-id="994ea-534">float4x2</span><span class="sxs-lookup"><span data-stu-id="994ea-534">float4x2</span></span>        | <span data-ttu-id="994ea-535">Dois 4D flutuantes.</span><span class="sxs-lookup"><span data-stu-id="994ea-535">Two 4D floats.</span></span>                               |
| <span data-ttu-id="994ea-536">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="994ea-536">PixelShaderConstant3</span></span>  | <span data-ttu-id="994ea-537">float4x3</span><span class="sxs-lookup"><span data-stu-id="994ea-537">float4x3</span></span>        | <span data-ttu-id="994ea-538">Três o 4D floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-538">Three 4D floats.</span></span>                             |
| <span data-ttu-id="994ea-539">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="994ea-539">PixelShaderConstant4</span></span>  | <span data-ttu-id="994ea-540">float4x4</span><span class="sxs-lookup"><span data-stu-id="994ea-540">float4x4</span></span>        | <span data-ttu-id="994ea-541">Quatro o 4D flutua.</span><span class="sxs-lookup"><span data-stu-id="994ea-541">Four 4D floats.</span></span>                              |
| <span data-ttu-id="994ea-542">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="994ea-542">PixelShaderConstantB</span></span>  | <span data-ttu-id="994ea-543">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-543">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="994ea-544">matriz m x n de BOOLs; m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-544">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="994ea-545">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="994ea-545">PixelShaderConstantI</span></span>  | <span data-ttu-id="994ea-546">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-546">int\[m\[n\]\]</span></span>   | <span data-ttu-id="994ea-547">matriz m x n de ints.</span><span class="sxs-lookup"><span data-stu-id="994ea-547">m x n array of ints.</span></span> <span data-ttu-id="994ea-548">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-548">m and n are optional.</span></span>   |
| <span data-ttu-id="994ea-549">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="994ea-549">PixelShaderConstantF</span></span>  | <span data-ttu-id="994ea-550">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-550">float\[m\[n\]\]</span></span> | <span data-ttu-id="994ea-551">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-551">m x n array of floats.</span></span> <span data-ttu-id="994ea-552">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-552">m and n are optional.</span></span> |
| <span data-ttu-id="994ea-553">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="994ea-553">VertexShaderConstant</span></span>  | <span data-ttu-id="994ea-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="994ea-555">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-555">m x n array of floats.</span></span> <span data-ttu-id="994ea-556">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-556">m and n are optional.</span></span> |
| <span data-ttu-id="994ea-557">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="994ea-557">VertexShaderConstant1</span></span> | <span data-ttu-id="994ea-558">float4</span><span class="sxs-lookup"><span data-stu-id="994ea-558">float4</span></span>          | <span data-ttu-id="994ea-559">Um 4D flutuante.</span><span class="sxs-lookup"><span data-stu-id="994ea-559">One 4D float.</span></span>                                |
| <span data-ttu-id="994ea-560">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="994ea-560">VertexShaderConstant2</span></span> | <span data-ttu-id="994ea-561">float4x2</span><span class="sxs-lookup"><span data-stu-id="994ea-561">float4x2</span></span>        | <span data-ttu-id="994ea-562">Dois 4D flutuantes.</span><span class="sxs-lookup"><span data-stu-id="994ea-562">Two 4D floats.</span></span>                               |
| <span data-ttu-id="994ea-563">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="994ea-563">VertexShaderConstant3</span></span> | <span data-ttu-id="994ea-564">float4x3</span><span class="sxs-lookup"><span data-stu-id="994ea-564">float4x3</span></span>        | <span data-ttu-id="994ea-565">Três o 4D floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-565">Three 4D floats.</span></span>                             |
| <span data-ttu-id="994ea-566">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="994ea-566">VertexShaderConstant4</span></span> | <span data-ttu-id="994ea-567">float4x4</span><span class="sxs-lookup"><span data-stu-id="994ea-567">float4x4</span></span>        | <span data-ttu-id="994ea-568">Quatro o 4D flutua.</span><span class="sxs-lookup"><span data-stu-id="994ea-568">Four 4D floats.</span></span>                              |
| <span data-ttu-id="994ea-569">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="994ea-569">VertexShaderConstantB</span></span> | <span data-ttu-id="994ea-570">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-570">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="994ea-571">matriz m x n de BOOLs.</span><span class="sxs-lookup"><span data-stu-id="994ea-571">m x n array of bools.</span></span> <span data-ttu-id="994ea-572">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-572">m and n are optional.</span></span>  |
| <span data-ttu-id="994ea-573">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="994ea-573">VertexShaderConstantI</span></span> | <span data-ttu-id="994ea-574">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-574">int\[m\[n\]\]</span></span>   | <span data-ttu-id="994ea-575">matriz m x n de ints.</span><span class="sxs-lookup"><span data-stu-id="994ea-575">m x n array of ints.</span></span> <span data-ttu-id="994ea-576">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-576">m and n are optional.</span></span>   |
| <span data-ttu-id="994ea-577">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="994ea-577">VertexShaderConstantF</span></span> | <span data-ttu-id="994ea-578">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="994ea-578">float\[m\[n\]\]</span></span> | <span data-ttu-id="994ea-579">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-579">m x n array of floats.</span></span> <span data-ttu-id="994ea-580">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="994ea-580">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="994ea-581">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="994ea-581">Texture States</span></span>

<span data-ttu-id="994ea-582">Os Estados de textura inicializam texturas usadas pelo misturador multitextura.</span><span class="sxs-lookup"><span data-stu-id="994ea-582">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="994ea-583">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="994ea-583">Texture State</span></span> | <span data-ttu-id="994ea-584">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-584">Type</span></span>    | <span data-ttu-id="994ea-585">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-585">Values</span></span>                            |
| <span data-ttu-id="994ea-586">Textura \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-586">Texture\[8\]</span></span>  | <span data-ttu-id="994ea-587">textura</span><span class="sxs-lookup"><span data-stu-id="994ea-587">texture</span></span> | <span data-ttu-id="994ea-588">**NULL** ou um parâmetro de textura.</span><span class="sxs-lookup"><span data-stu-id="994ea-588">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="994ea-589">Estados de estágio de textura</span><span class="sxs-lookup"><span data-stu-id="994ea-589">Texture Stage States</span></span>

<span data-ttu-id="994ea-590">Estados de estágio de textura configuram texturas e os estágios de textura no misturador multitextura.</span><span class="sxs-lookup"><span data-stu-id="994ea-590">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994ea-591">Estado do estágio de textura</span><span class="sxs-lookup"><span data-stu-id="994ea-591">Texture Stage State</span></span>        | <span data-ttu-id="994ea-592">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-592">Type</span></span>  | <span data-ttu-id="994ea-593">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-593">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="994ea-594">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-594">AlphaOp\[8\]</span></span>               | <span data-ttu-id="994ea-595">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-595">dword</span></span> | <span data-ttu-id="994ea-596">O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="994ea-596">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="994ea-597">Consulte D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="994ea-597">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="994ea-598">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-598">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="994ea-599">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-599">dword</span></span> | <span data-ttu-id="994ea-600">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-600">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-601">Consulte D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="994ea-601">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="994ea-602">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-602">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="994ea-603">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-603">dword</span></span> | <span data-ttu-id="994ea-604">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-605">Consulte D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="994ea-605">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="994ea-606">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-606">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="994ea-607">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-607">dword</span></span> | <span data-ttu-id="994ea-608">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-609">Consulte D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="994ea-609">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="994ea-610">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-610">ColorArg0\[8\]</span></span>             | <span data-ttu-id="994ea-611">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-611">dword</span></span> | <span data-ttu-id="994ea-612">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-613">Consulte D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="994ea-613">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="994ea-614">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-614">ColorArg1\[8\]</span></span>             | <span data-ttu-id="994ea-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-615">dword</span></span> | <span data-ttu-id="994ea-616">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-617">Consulte D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="994ea-617">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="994ea-618">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-618">ColorArg2\[8\]</span></span>             | <span data-ttu-id="994ea-619">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-619">dword</span></span> | <span data-ttu-id="994ea-620">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-621">Consulte D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="994ea-621">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="994ea-622">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-622">ColorOp\[8\]</span></span>               | <span data-ttu-id="994ea-623">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-623">dword</span></span> | <span data-ttu-id="994ea-624">O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="994ea-624">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="994ea-625">Consulte D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="994ea-625">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="994ea-626">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-626">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="994ea-627">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-627">float</span></span> | <span data-ttu-id="994ea-628">Os mesmos valores que D3DTSS \_ BUMPENVLSCALE sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="994ea-628">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="994ea-629">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-629">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="994ea-630">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-630">float</span></span> | <span data-ttu-id="994ea-631">Os mesmos valores que D3DTSS \_ BUMPENVLOFFSET sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="994ea-631">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="994ea-632">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-632">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="994ea-633">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-633">float</span></span> | <span data-ttu-id="994ea-634">Mesmos valores que D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="994ea-634">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="994ea-635">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-635">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="994ea-636">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-636">float</span></span> | <span data-ttu-id="994ea-637">Mesmos valores que D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="994ea-637">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="994ea-638">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-638">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="994ea-639">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-639">float</span></span> | <span data-ttu-id="994ea-640">Mesmos valores que D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="994ea-640">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="994ea-641">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-641">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="994ea-642">FLOAT</span><span class="sxs-lookup"><span data-stu-id="994ea-642">float</span></span> | <span data-ttu-id="994ea-643">Mesmos valores que D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="994ea-643">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="994ea-644">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-644">ResultArg\[8\]</span></span>             | <span data-ttu-id="994ea-645">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-645">dword</span></span> | <span data-ttu-id="994ea-646">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="994ea-646">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="994ea-647">Consulte D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="994ea-647">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="994ea-648">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-648">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="994ea-649">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-649">dword</span></span> | <span data-ttu-id="994ea-650">Os mesmos valores que D3DTSS \_ TEXCOORDINDEX sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="994ea-650">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="994ea-651">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-651">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="994ea-652">DWORD</span><span class="sxs-lookup"><span data-stu-id="994ea-652">dword</span></span> | <span data-ttu-id="994ea-653">Mesmos valores que [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) valores sem o \_ prefixo D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="994ea-653">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="994ea-654">Consulte D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="994ea-654">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="994ea-655">Estados de transformação</span><span class="sxs-lookup"><span data-stu-id="994ea-655">Transform States</span></span>

<span data-ttu-id="994ea-656">Defina Estados de transformação para inicializar matrizes de transformação.</span><span class="sxs-lookup"><span data-stu-id="994ea-656">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="994ea-657">Os efeitos usam matrizes transpostas para obter eficiência.</span><span class="sxs-lookup"><span data-stu-id="994ea-657">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="994ea-658">Você pode fornecer matrizes transpostas a um efeito, ou um efeito irá transpor automaticamente as matrizes antes de usá-las.</span><span class="sxs-lookup"><span data-stu-id="994ea-658">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994ea-659">Estado de transformação</span><span class="sxs-lookup"><span data-stu-id="994ea-659">Transform State</span></span>       | <span data-ttu-id="994ea-660">Type</span><span class="sxs-lookup"><span data-stu-id="994ea-660">Type</span></span>     | <span data-ttu-id="994ea-661">Valores</span><span class="sxs-lookup"><span data-stu-id="994ea-661">Values</span></span>                                                                                                                          |
| <span data-ttu-id="994ea-662">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="994ea-662">ProjectionTransform</span></span>   | <span data-ttu-id="994ea-663">float4x4</span><span class="sxs-lookup"><span data-stu-id="994ea-663">float4x4</span></span> | <span data-ttu-id="994ea-664">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-664">A 4x4 matrix of floats.</span></span> <span data-ttu-id="994ea-665">Mesmos valores que D3DTS \_ projeção sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="994ea-665">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="994ea-666">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="994ea-666">TextureTransform\[8\]</span></span> | <span data-ttu-id="994ea-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="994ea-667">float4x4</span></span> | <span data-ttu-id="994ea-668">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="994ea-669">Mesmos valores que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="994ea-669">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="994ea-670">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="994ea-670">ViewTransform</span></span>         | <span data-ttu-id="994ea-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="994ea-671">float4x4</span></span> | <span data-ttu-id="994ea-672">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="994ea-673">Mesmos valores que D3DTS \_ exibição sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="994ea-673">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="994ea-674">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="994ea-674">WorldTransform</span></span>        | <span data-ttu-id="994ea-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="994ea-675">float4x4</span></span> | <span data-ttu-id="994ea-676">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="994ea-676">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="994ea-677">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="994ea-677">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="994ea-678">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="994ea-678">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
