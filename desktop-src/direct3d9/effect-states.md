---
description: Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe92661fda82bd7dfa47ead0061ef8606e422a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998863"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="10887-103">Estados de efeito (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10887-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="10887-104">Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.</span><span class="sxs-lookup"><span data-stu-id="10887-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="10887-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="10887-105">Where:</span></span>

-   <span data-ttu-id="10887-106">Estado de efeito – semelhante aos Estados de pipeline de função fixa tradicional.</span><span class="sxs-lookup"><span data-stu-id="10887-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="10887-107">Uma lista completa de Estados é fornecida abaixo.</span><span class="sxs-lookup"><span data-stu-id="10887-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="10887-108">\[\[ \] índice \] do -Índice inteiro opcional.</span><span class="sxs-lookup"><span data-stu-id="10887-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="10887-109">O índice identifica um estado específico dentro de uma matriz de Estados de efeito.</span><span class="sxs-lookup"><span data-stu-id="10887-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="10887-110">Os colchetes externos indicam que um índice é opcional.</span><span class="sxs-lookup"><span data-stu-id="10887-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="10887-111">Se um índice for usado, certifique-se de usar os colchetes internos.</span><span class="sxs-lookup"><span data-stu-id="10887-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="10887-112">Expression – expressão de atribuição de estado.</span><span class="sxs-lookup"><span data-stu-id="10887-112">expression - State assignment expression.</span></span> <span data-ttu-id="10887-113">Consulte [Expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="10887-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="10887-114">Cada Estado tem um tipo de dados nativo.</span><span class="sxs-lookup"><span data-stu-id="10887-114">Each state has a native data type.</span></span> <span data-ttu-id="10887-115">Esse é o tipo de dados em que o estado espera que os valores estejam quando o efeito os atribui.</span><span class="sxs-lookup"><span data-stu-id="10887-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="10887-116">Os tipos de dados esperados por cada Estado estão listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="10887-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="10887-117">Observe que a interface de efeito tentará converter valores para o tipo apropriado o mais cedo possível.</span><span class="sxs-lookup"><span data-stu-id="10887-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="10887-118">Valores literais podem ser convertidos em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="10887-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="10887-119">Não literais (ou seja, variáveis regulares) precisam ser convertidas quando os métodos definidos apropriados são chamados.</span><span class="sxs-lookup"><span data-stu-id="10887-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="10887-120">Por exemplo, a interface de efeito converterá valores definidos usando [**setbool**](id3dxbaseeffect--setbool.md), [**DefinirValor**](id3dxbaseeffect--setvalue.md)e outras funções semelhantes, se necessário.</span><span class="sxs-lookup"><span data-stu-id="10887-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="10887-121">Para melhorar o desempenho, verifique se os valores passados para a interface de efeito já são do tipo correto e não precisarão de conversão.</span><span class="sxs-lookup"><span data-stu-id="10887-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="10887-122">Se o tempo de execução não puder converter um valor, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="10887-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="10887-123">Os Estados de efeito podem ser divididos nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="10887-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="10887-124">Estados claros</span><span class="sxs-lookup"><span data-stu-id="10887-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="10887-125">Estados de material</span><span class="sxs-lookup"><span data-stu-id="10887-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="10887-126">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="10887-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="10887-127">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="10887-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="10887-128">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="10887-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="10887-129">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="10887-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="10887-130">Estados de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="10887-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="10887-131">Estados do sombreador</span><span class="sxs-lookup"><span data-stu-id="10887-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="10887-132">Estados de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="10887-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="10887-133">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="10887-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="10887-134">Estados de estágio de textura</span><span class="sxs-lookup"><span data-stu-id="10887-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="10887-135">Estados de transformação</span><span class="sxs-lookup"><span data-stu-id="10887-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="10887-136">Estados claros</span><span class="sxs-lookup"><span data-stu-id="10887-136">Light States</span></span>

<span data-ttu-id="10887-137">Para habilitar o melhor desempenho para a aplicação de um efeito, todos os componentes de uma luz ou um material devem ser especificados no arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="10887-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="10887-138">Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de luz individualmente.</span><span class="sxs-lookup"><span data-stu-id="10887-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



| <span data-ttu-id="10887-139">Estado claro</span><span class="sxs-lookup"><span data-stu-id="10887-139">Light State</span></span>            | <span data-ttu-id="10887-140">Type</span><span class="sxs-lookup"><span data-stu-id="10887-140">Type</span></span>   | <span data-ttu-id="10887-141">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-141">Values</span></span>                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10887-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="10887-143">float4</span><span class="sxs-lookup"><span data-stu-id="10887-143">float4</span></span> | <span data-ttu-id="10887-144">Consulte o membro de ambiente de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="10887-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="10887-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-146">float</span></span>  | <span data-ttu-id="10887-147">Consulte o membro Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="10887-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="10887-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-149">float</span></span>  | <span data-ttu-id="10887-150">Consulte o membro Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="10887-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="10887-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-152">float</span></span>  | <span data-ttu-id="10887-153">Consulte o membro Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="10887-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="10887-155">float4</span><span class="sxs-lookup"><span data-stu-id="10887-155">float4</span></span> | <span data-ttu-id="10887-156">Consulte o membro difuso de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="10887-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="10887-158">float3</span><span class="sxs-lookup"><span data-stu-id="10887-158">float3</span></span> | <span data-ttu-id="10887-159">Consulte o membro de direção de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="10887-160">N mais claro \[\]</span><span class="sxs-lookup"><span data-stu-id="10887-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="10887-161">bool</span><span class="sxs-lookup"><span data-stu-id="10887-161">bool</span></span>   | <span data-ttu-id="10887-162">**True** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="10887-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="10887-163">Consulte o argumento bEnable em [**clarear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="10887-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="10887-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="10887-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-165">float</span></span>  | <span data-ttu-id="10887-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="10887-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="10887-167">Consulte o membro de queda de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="10887-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="10887-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-169">float</span></span>  | <span data-ttu-id="10887-170">Consulte o membro Phi de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="10887-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="10887-172">float3</span><span class="sxs-lookup"><span data-stu-id="10887-172">float3</span></span> | <span data-ttu-id="10887-173">Consulte o membro position de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="10887-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-174">LightRange\[n\]</span></span>        | <span data-ttu-id="10887-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-175">float</span></span>  | <span data-ttu-id="10887-176">Consulte o membro Range de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="10887-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="10887-178">float4</span><span class="sxs-lookup"><span data-stu-id="10887-178">float4</span></span> | <span data-ttu-id="10887-179">Consulte o membro especular de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="10887-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="10887-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-181">float</span></span>  | <span data-ttu-id="10887-182">Consulte o membro teta de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="10887-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="10887-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="10887-183">LightType\[n\]</span></span>         | <span data-ttu-id="10887-184">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-184">dword</span></span>  | <span data-ttu-id="10887-185">Mesmo valor que a matriz de até n valores de [**D3DLIGHTTYPE**](./d3dlighttype.md) sem o \_ prefixo D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="10887-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="10887-186">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="10887-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="10887-187">Isso habilitará a iluminação, tornará a iluminação do tipo, definirá a posição da luz como float3<10.0 f, 1,0 f, 23.0 f> e definirá a cor do ambiente como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1.0>.</span><span class="sxs-lookup"><span data-stu-id="10887-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="10887-188">Estados de material</span><span class="sxs-lookup"><span data-stu-id="10887-188">Material States</span></span>

<span data-ttu-id="10887-189">Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de material individualmente.</span><span class="sxs-lookup"><span data-stu-id="10887-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



| <span data-ttu-id="10887-190">Estado do material</span><span class="sxs-lookup"><span data-stu-id="10887-190">Material State</span></span>   | <span data-ttu-id="10887-191">Type</span><span class="sxs-lookup"><span data-stu-id="10887-191">Type</span></span>   | <span data-ttu-id="10887-192">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-192">Values</span></span>                                         |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="10887-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="10887-193">MaterialAmbient</span></span>  | <span data-ttu-id="10887-194">float4</span><span class="sxs-lookup"><span data-stu-id="10887-194">float4</span></span> | <span data-ttu-id="10887-195">Mesmo valor que o [ **ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="10887-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="10887-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="10887-196">MaterialDiffuse</span></span>  | <span data-ttu-id="10887-197">float4</span><span class="sxs-lookup"><span data-stu-id="10887-197">float4</span></span> | <span data-ttu-id="10887-198">Mesmo valor que [ **difusa**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="10887-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="10887-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="10887-199">MaterialEmissive</span></span> | <span data-ttu-id="10887-200">float4</span><span class="sxs-lookup"><span data-stu-id="10887-200">float4</span></span> | <span data-ttu-id="10887-201">Mesmo valor que [ **emissiva**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="10887-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="10887-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="10887-202">MaterialPower</span></span>    | <span data-ttu-id="10887-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-203">float</span></span>  | <span data-ttu-id="10887-204">Mesmo valor que a [ **energia**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="10887-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="10887-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="10887-205">MaterialSpecular</span></span> | <span data-ttu-id="10887-206">float4</span><span class="sxs-lookup"><span data-stu-id="10887-206">float4</span></span> | <span data-ttu-id="10887-207">Mesmo valor que [ **especular**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="10887-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="10887-208">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="10887-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="10887-209">Isso definirá a cor difusa como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f> e tornará o poder do material 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="10887-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="10887-210">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="10887-210">Render States</span></span>

<span data-ttu-id="10887-211">Há dois tipos de Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="10887-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="10887-212">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="10887-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="10887-213">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="10887-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="10887-214">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="10887-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="10887-215">Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="10887-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10887-216">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="10887-216">Render State</span></span></td>
<td><span data-ttu-id="10887-217">Type</span><span class="sxs-lookup"><span data-stu-id="10887-217">Type</span></span></td>
<td><span data-ttu-id="10887-218">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="10887-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="10887-220">bool</span><span class="sxs-lookup"><span data-stu-id="10887-220">bool</span></span></td>
<td><span data-ttu-id="10887-221">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-221">True or False.</span></span> <span data-ttu-id="10887-222">Os mesmos valores que D3DRS_ALPHABLENDENABLE em <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="10887-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="10887-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="10887-224">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-224">dword</span></span></td>
<td><span data-ttu-id="10887-225">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="10887-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="10887-226">Consulte D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="10887-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="10887-227">AlphaRef</span></span></td>
<td><span data-ttu-id="10887-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-228">dword</span></span></td>
<td><span data-ttu-id="10887-229">Mesmos valores que D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="10887-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="10887-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="10887-231">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-231">dword</span></span></td>
<td><span data-ttu-id="10887-232">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-232">True or False.</span></span> <span data-ttu-id="10887-233">Consulte D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="10887-234">BlendOp</span></span></td>
<td><span data-ttu-id="10887-235">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-235">dword</span></span></td>
<td><span data-ttu-id="10887-236">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sem o prefixo D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="10887-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="10887-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="10887-238">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-238">dword</span></span></td>
<td><span data-ttu-id="10887-239">Combinação de bits de vermelho | VERDE | AZUL | Alfa.</span><span class="sxs-lookup"><span data-stu-id="10887-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="10887-240">Consulte D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="10887-241">DepthBias</span></span></td>
<td><span data-ttu-id="10887-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-242">float</span></span></td>
<td><span data-ttu-id="10887-243">Mesmos valores que D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="10887-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="10887-244">DestBlend</span></span></td>
<td><span data-ttu-id="10887-245">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-245">dword</span></span></td>
<td><span data-ttu-id="10887-246">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="10887-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="10887-247">DitherEnable</span></span></td>
<td><span data-ttu-id="10887-248">bool</span><span class="sxs-lookup"><span data-stu-id="10887-248">bool</span></span></td>
<td><span data-ttu-id="10887-249">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-249">True or False.</span></span> <span data-ttu-id="10887-250">Mesmos valores que D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="10887-251">FillMode</span></span></td>
<td><span data-ttu-id="10887-252">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-252">dword</span></span></td>
<td><span data-ttu-id="10887-253">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sem o prefixo D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="10887-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="10887-254">LastPixel</span></span></td>
<td><span data-ttu-id="10887-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-255">dword</span></span></td>
<td><span data-ttu-id="10887-256">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-256">True or False.</span></span> <span data-ttu-id="10887-257">Consulte D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="10887-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-258">Shadmode</span><span class="sxs-lookup"><span data-stu-id="10887-258">ShadeMode</span></span></td>
<td><span data-ttu-id="10887-259">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-259">dword</span></span></td>
<td><span data-ttu-id="10887-260">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sem o prefixo D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="10887-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="10887-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="10887-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-262">float</span></span></td>
<td><span data-ttu-id="10887-263">Mesmos valores que D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="10887-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="10887-264">SrcBlend</span></span></td>
<td><span data-ttu-id="10887-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-265">dword</span></span></td>
<td><span data-ttu-id="10887-266">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="10887-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="10887-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="10887-268">bool</span><span class="sxs-lookup"><span data-stu-id="10887-268">bool</span></span></td>
<td><span data-ttu-id="10887-269">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-269">True or False.</span></span> <span data-ttu-id="10887-270">Mesmos valores que D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="10887-271">StencilEnable</span></span></td>
<td><span data-ttu-id="10887-272">bool</span><span class="sxs-lookup"><span data-stu-id="10887-272">bool</span></span></td>
<td><span data-ttu-id="10887-273">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-273">True or False.</span></span> <span data-ttu-id="10887-274">Mesmos valores que D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="10887-275">StencilFail</span></span></td>
<td><span data-ttu-id="10887-276">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-276">dword</span></span></td>
<td><span data-ttu-id="10887-277">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="10887-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="10887-278">Consulte D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="10887-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="10887-279">StencilFunc</span></span></td>
<td><span data-ttu-id="10887-280">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-280">dword</span></span></td>
<td><span data-ttu-id="10887-281">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="10887-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="10887-282">Consulte D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="10887-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="10887-283">StencilMask</span></span></td>
<td><span data-ttu-id="10887-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-284">dword</span></span></td>
<td><span data-ttu-id="10887-285">Mesmos valores que D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="10887-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="10887-286">StencilPass</span></span></td>
<td><span data-ttu-id="10887-287">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-287">dword</span></span></td>
<td><span data-ttu-id="10887-288">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="10887-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="10887-289">Consulte D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="10887-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="10887-290">StencilRef</span></span></td>
<td><span data-ttu-id="10887-291">INT</span><span class="sxs-lookup"><span data-stu-id="10887-291">int</span></span></td>
<td><span data-ttu-id="10887-292">Mesmos valores que D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="10887-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="10887-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="10887-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-294">dword</span></span></td>
<td><span data-ttu-id="10887-295">Mesmos valores que D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="10887-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="10887-296">StencilZFail</span></span></td>
<td><span data-ttu-id="10887-297">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-297">dword</span></span></td>
<td><span data-ttu-id="10887-298">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="10887-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="10887-299">Consulte D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="10887-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="10887-300">TextureFactor</span></span></td>
<td><span data-ttu-id="10887-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-301">dword</span></span></td>
<td><span data-ttu-id="10887-302">Mesmos valores que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="10887-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="10887-303">Mesmos valores que D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="10887-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="10887-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="10887-305">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-305">dword</span></span></td>
<td><span data-ttu-id="10887-306">Os valores são os mesmos que os valores usados pelo D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="10887-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="10887-307">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="10887-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="10887-308">COORD0 (que corresponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="10887-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="10887-309">COORD1 (que corresponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="10887-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="10887-310">COORD2 (que corresponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="10887-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="10887-311">COORD3 (que corresponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="10887-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="10887-312">U (que corresponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="10887-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="10887-313">V (que corresponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="10887-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="10887-314">W (que corresponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="10887-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="10887-315">ZEnable</span></span></td>
<td><span data-ttu-id="10887-316">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-316">dword</span></span></td>
<td><span data-ttu-id="10887-317">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sem o prefixo D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="10887-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10887-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="10887-318">ZFunc</span></span></td>
<td><span data-ttu-id="10887-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-319">dword</span></span></td>
<td><span data-ttu-id="10887-320">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="10887-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="10887-321">Consulte D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="10887-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10887-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="10887-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="10887-323">bool</span><span class="sxs-lookup"><span data-stu-id="10887-323">bool</span></span></td>
<td><span data-ttu-id="10887-324">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-324">True or False.</span></span> <span data-ttu-id="10887-325">Consulte D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="10887-326">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="10887-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="10887-327">Isso habilitará a mistura alfa e fará com que todas as geometrias sejam renderizadas em wireframe.</span><span class="sxs-lookup"><span data-stu-id="10887-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="10887-328">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="10887-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="10887-329">Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="10887-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



| <span data-ttu-id="10887-330">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="10887-330">Render State</span></span>             | <span data-ttu-id="10887-331">Type</span><span class="sxs-lookup"><span data-stu-id="10887-331">Type</span></span>   | <span data-ttu-id="10887-332">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-332">Values</span></span>                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10887-333">Ambiente</span><span class="sxs-lookup"><span data-stu-id="10887-333">Ambient</span></span>                  | <span data-ttu-id="10887-334">float4</span><span class="sxs-lookup"><span data-stu-id="10887-334">float4</span></span> | <span data-ttu-id="10887-335">Mesmos valores que D3DRS \_ ambiente.</span><span class="sxs-lookup"><span data-stu-id="10887-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="10887-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="10887-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="10887-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-337">dword</span></span>  | <span data-ttu-id="10887-338">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="10887-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="10887-339">Consulte D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="10887-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="10887-340">Recortando</span><span class="sxs-lookup"><span data-stu-id="10887-340">Clipping</span></span>                 | <span data-ttu-id="10887-341">bool</span><span class="sxs-lookup"><span data-stu-id="10887-341">bool</span></span>   | <span data-ttu-id="10887-342">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-342">True or False.</span></span> <span data-ttu-id="10887-343">Mesmos valores que o \_ recorte de D3DRS.</span><span class="sxs-lookup"><span data-stu-id="10887-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="10887-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="10887-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="10887-345">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-345">dword</span></span>  | <span data-ttu-id="10887-346">Combinação de bits de D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="10887-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="10887-347">Consulte [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="10887-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="10887-348">ColorVertex</span></span>              | <span data-ttu-id="10887-349">bool</span><span class="sxs-lookup"><span data-stu-id="10887-349">bool</span></span>   | <span data-ttu-id="10887-350">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-350">True or False.</span></span> <span data-ttu-id="10887-351">Mesmos valores que D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="10887-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="10887-352">De seleção</span><span class="sxs-lookup"><span data-stu-id="10887-352">CullMode</span></span>                 | <span data-ttu-id="10887-353">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-353">dword</span></span>  | <span data-ttu-id="10887-354">Mesmos valores que [**D3DCULL**](./d3dcull.md) sem o \_ prefixo D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="10887-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="10887-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="10887-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="10887-356">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-356">dword</span></span>  | <span data-ttu-id="10887-357">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="10887-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="10887-358">Consulte D3DRS \_ DiffuseMaterialSource.</span><span class="sxs-lookup"><span data-stu-id="10887-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="10887-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="10887-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="10887-360">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-360">dword</span></span>  | <span data-ttu-id="10887-361">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="10887-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="10887-362">Consulte D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="10887-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="10887-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="10887-363">FogColor</span></span>                 | <span data-ttu-id="10887-364">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-364">dword</span></span>  | <span data-ttu-id="10887-365">Mesmos valores que [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="10887-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="10887-366">Consulte D3DRS \_ FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="10887-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="10887-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="10887-367">FogDensity</span></span>               | <span data-ttu-id="10887-368">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-368">float</span></span>  | <span data-ttu-id="10887-369">Mesmos valores que D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="10887-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="10887-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="10887-370">FogEnable</span></span>                | <span data-ttu-id="10887-371">bool</span><span class="sxs-lookup"><span data-stu-id="10887-371">bool</span></span>   | <span data-ttu-id="10887-372">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-372">True or False.</span></span> <span data-ttu-id="10887-373">Mesmos valores que D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="10887-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="10887-374">FogEnd</span></span>                   | <span data-ttu-id="10887-375">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-375">float</span></span>  | <span data-ttu-id="10887-376">Mesmos valores que D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="10887-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="10887-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="10887-377">FogStart</span></span>                 | <span data-ttu-id="10887-378">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-378">float</span></span>  | <span data-ttu-id="10887-379">Mesmos valores que D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="10887-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="10887-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="10887-380">FogTableMode</span></span>             | <span data-ttu-id="10887-381">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-381">dword</span></span>  | <span data-ttu-id="10887-382">Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="10887-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="10887-383">Consulte D3DRS \_ FOGTABLEMODE no [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="10887-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="10887-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="10887-384">FogVertexMode</span></span>            | <span data-ttu-id="10887-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-385">dword</span></span>  | <span data-ttu-id="10887-386">Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md) sem o \_ prefixo D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="10887-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="10887-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="10887-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="10887-388">bool</span><span class="sxs-lookup"><span data-stu-id="10887-388">bool</span></span>   | <span data-ttu-id="10887-389">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-389">True or False.</span></span> <span data-ttu-id="10887-390">Mesmos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="10887-391">Iluminação</span><span class="sxs-lookup"><span data-stu-id="10887-391">Lighting</span></span>                 | <span data-ttu-id="10887-392">bool</span><span class="sxs-lookup"><span data-stu-id="10887-392">bool</span></span>   | <span data-ttu-id="10887-393">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-393">True or False.</span></span> <span data-ttu-id="10887-394">Mesmos valores que a \_ iluminação D3DRS.</span><span class="sxs-lookup"><span data-stu-id="10887-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="10887-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="10887-395">LocalViewer</span></span>              | <span data-ttu-id="10887-396">bool</span><span class="sxs-lookup"><span data-stu-id="10887-396">bool</span></span>   | <span data-ttu-id="10887-397">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-397">True or False.</span></span> <span data-ttu-id="10887-398">Mesmos valores que D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="10887-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="10887-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="10887-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="10887-400">bool</span><span class="sxs-lookup"><span data-stu-id="10887-400">bool</span></span>   | <span data-ttu-id="10887-401">Mesmos valores que D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="10887-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="10887-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="10887-402">MultiSampleMask</span></span>          | <span data-ttu-id="10887-403">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-403">dword</span></span>  | <span data-ttu-id="10887-404">Mesmos valores que D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="10887-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="10887-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="10887-405">NormalizeNormals</span></span>         | <span data-ttu-id="10887-406">bool</span><span class="sxs-lookup"><span data-stu-id="10887-406">bool</span></span>   | <span data-ttu-id="10887-407">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-407">True or False.</span></span> <span data-ttu-id="10887-408">Mesmos valores que D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="10887-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="10887-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="10887-409">PatchSegments</span></span>            | <span data-ttu-id="10887-410">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-410">float</span></span>  | <span data-ttu-id="10887-411">Mesmos valores que nSegments em [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="10887-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="10887-412">PointScale \_ A</span><span class="sxs-lookup"><span data-stu-id="10887-412">PointScale\_A</span></span>            | <span data-ttu-id="10887-413">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-413">float</span></span>  | <span data-ttu-id="10887-414">Os mesmos valores que D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="10887-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="10887-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="10887-415">PointScale\_B</span></span>            | <span data-ttu-id="10887-416">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-416">float</span></span>  | <span data-ttu-id="10887-417">Os mesmos valores que D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="10887-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="10887-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="10887-418">PointScale\_C</span></span>            | <span data-ttu-id="10887-419">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-419">float</span></span>  | <span data-ttu-id="10887-420">Os mesmos valores que D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="10887-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="10887-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="10887-421">PointScaleEnable</span></span>         | <span data-ttu-id="10887-422">bool</span><span class="sxs-lookup"><span data-stu-id="10887-422">bool</span></span>   | <span data-ttu-id="10887-423">Mesmos valores que D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="10887-424">Pontos</span><span class="sxs-lookup"><span data-stu-id="10887-424">PointSize</span></span>                | <span data-ttu-id="10887-425">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-425">float</span></span>  | <span data-ttu-id="10887-426">Os mesmos valores que D3DRS \_ apontam.</span><span class="sxs-lookup"><span data-stu-id="10887-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="10887-427">Pontos \_ mínimos</span><span class="sxs-lookup"><span data-stu-id="10887-427">PointSize\_Min</span></span>           | <span data-ttu-id="10887-428">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-428">float</span></span>  | <span data-ttu-id="10887-429">Os mesmos valores que D3DRS \_ apontam \_ mín.</span><span class="sxs-lookup"><span data-stu-id="10887-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="10887-430">Pontos \_ máximos</span><span class="sxs-lookup"><span data-stu-id="10887-430">PointSize\_Max</span></span>           | <span data-ttu-id="10887-431">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-431">float</span></span>  | <span data-ttu-id="10887-432">Os mesmos valores que D3DRS \_ aponta para \_ Max sem o \_ prefixo D3DRS.</span><span class="sxs-lookup"><span data-stu-id="10887-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="10887-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="10887-433">PointSpriteEnable</span></span>        | <span data-ttu-id="10887-434">bool</span><span class="sxs-lookup"><span data-stu-id="10887-434">bool</span></span>   | <span data-ttu-id="10887-435">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-435">True or False.</span></span> <span data-ttu-id="10887-436">Mesmos valores que D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="10887-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="10887-437">RangeFogEnable</span></span>           | <span data-ttu-id="10887-438">bool</span><span class="sxs-lookup"><span data-stu-id="10887-438">bool</span></span>   | <span data-ttu-id="10887-439">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-439">True or False.</span></span> <span data-ttu-id="10887-440">Mesmos valores que D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="10887-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="10887-441">SpecularEnable</span></span>           | <span data-ttu-id="10887-442">bool</span><span class="sxs-lookup"><span data-stu-id="10887-442">bool</span></span>   | <span data-ttu-id="10887-443">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="10887-443">True or False.</span></span> <span data-ttu-id="10887-444">Mesmos valores que D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="10887-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="10887-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="10887-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="10887-446">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-446">dword</span></span>  | <span data-ttu-id="10887-447">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="10887-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="10887-448">Consulte D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="10887-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="10887-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="10887-449">TweenFactor</span></span>              | <span data-ttu-id="10887-450">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-450">float</span></span>  | <span data-ttu-id="10887-451">Mesmos valores que D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="10887-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="10887-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="10887-452">VertexBlend</span></span>              | <span data-ttu-id="10887-453">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-453">dword</span></span>  | <span data-ttu-id="10887-454">Mesmos valores que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sem o \_ prefixo D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="10887-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="10887-455">Consulte D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="10887-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="10887-456">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="10887-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="10887-457">Isso fará com que a cor do ambiente FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f>, defina o modo de remoção do backface como contador no sentido anti-horário e defina a cor da neblina como vermelha.</span><span class="sxs-lookup"><span data-stu-id="10887-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="10887-458">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="10887-458">Sampler States</span></span>

<span data-ttu-id="10887-459">Um estado de amostra representa um objeto de amostra.</span><span class="sxs-lookup"><span data-stu-id="10887-459">A sampler state represents a sampler object.</span></span>



| <span data-ttu-id="10887-460">Estado</span><span class="sxs-lookup"><span data-stu-id="10887-460">State</span></span>   | <span data-ttu-id="10887-461">Type</span><span class="sxs-lookup"><span data-stu-id="10887-461">Type</span></span>    | <span data-ttu-id="10887-462">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-462">Values</span></span>                              |
|---------|---------|-------------------------------------|
| <span data-ttu-id="10887-463">Exemplo</span><span class="sxs-lookup"><span data-stu-id="10887-463">Sampler</span></span> | <span data-ttu-id="10887-464">cores</span><span class="sxs-lookup"><span data-stu-id="10887-464">sampler</span></span> | <span data-ttu-id="10887-465">**NULL** ou um bloco de estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="10887-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="10887-466">Estados de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="10887-466">Sampler Stage States</span></span>

<span data-ttu-id="10887-467">Os Estados de estágio de amostra são usados para amostras de texturas.</span><span class="sxs-lookup"><span data-stu-id="10887-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="10887-468">O estado de amostra determina os tipos de filtragem e os modos de endereçamento de textura.</span><span class="sxs-lookup"><span data-stu-id="10887-468">Sampler state determines filtering types and texture addressing modes.</span></span>



| <span data-ttu-id="10887-469">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="10887-469">Sampler State</span></span>       | <span data-ttu-id="10887-470">Type</span><span class="sxs-lookup"><span data-stu-id="10887-470">Type</span></span>                         | <span data-ttu-id="10887-471">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-471">Values</span></span>                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10887-472">Endereço de \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-472">AddressU\[16\]</span></span>      | <span data-ttu-id="10887-473">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-473">dword</span></span>                        | <span data-ttu-id="10887-474">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="10887-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="10887-475">Consulte D3DSAMP \_ AddressU.</span><span class="sxs-lookup"><span data-stu-id="10887-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="10887-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-476">AddressV\[16\]</span></span>      | <span data-ttu-id="10887-477">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-477">dword</span></span>                        | <span data-ttu-id="10887-478">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="10887-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="10887-479">Consulte D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="10887-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="10887-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-480">AddressW\[16\]</span></span>      | <span data-ttu-id="10887-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-481">dword</span></span>                        | <span data-ttu-id="10887-482">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="10887-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="10887-483">Consulte D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="10887-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="10887-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="10887-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="10887-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="10887-486">Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="10887-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="10887-487">Consulte D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="10887-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="10887-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="10887-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-489">dword</span></span>                        | <span data-ttu-id="10887-490">Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="10887-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="10887-491">Consulte D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="10887-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="10887-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="10887-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-493">dword</span></span>                        | <span data-ttu-id="10887-494">Os mesmos valores que D3DSAMP \_ MAXANISOTROPY sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="10887-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="10887-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="10887-496">INT</span><span class="sxs-lookup"><span data-stu-id="10887-496">int</span></span>                          | <span data-ttu-id="10887-497">Os mesmos valores que D3DSAMP \_ MAXMIPLEVEL sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="10887-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="10887-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="10887-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-499">dword</span></span>                        | <span data-ttu-id="10887-500">Os mesmos valores que D3DSAMP \_ MINFILTER sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="10887-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="10887-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="10887-502">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-502">dword</span></span>                        | <span data-ttu-id="10887-503">Os mesmos valores que D3DSAMP \_ MIPFILTER sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="10887-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="10887-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="10887-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="10887-505">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-505">float</span></span>                        | <span data-ttu-id="10887-506">Os mesmos valores que D3DSAMP \_ MIPMAPLODBIAS sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="10887-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="10887-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="10887-507">SRGBTexture</span></span>         | <span data-ttu-id="10887-508">bool</span><span class="sxs-lookup"><span data-stu-id="10887-508">bool</span></span>                         | <span data-ttu-id="10887-509">Mesmo valor que D3DSAMP \_ SRGBTEXTURE sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="10887-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="10887-510">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="10887-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="10887-511">Isso coloca UVW valores entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="10887-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="10887-512">Estados do sombreador</span><span class="sxs-lookup"><span data-stu-id="10887-512">Shader States</span></span>

<span data-ttu-id="10887-513">Há apenas dois Estados de sombreador de efeito: um associado a um objeto de sombreador de vértice e o outro associado a um objeto de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="10887-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



| <span data-ttu-id="10887-514">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="10887-514">Shader State</span></span> | <span data-ttu-id="10887-515">Type</span><span class="sxs-lookup"><span data-stu-id="10887-515">Type</span></span>         | <span data-ttu-id="10887-516">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-516">Values</span></span>                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="10887-517">PixelShader</span><span class="sxs-lookup"><span data-stu-id="10887-517">PixelShader</span></span>  | <span data-ttu-id="10887-518">PixelShader</span><span class="sxs-lookup"><span data-stu-id="10887-518">pixelshader</span></span>  | <span data-ttu-id="10887-519">**NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="10887-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="10887-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="10887-520">VertexShader</span></span> | <span data-ttu-id="10887-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="10887-521">vertexshader</span></span> | <span data-ttu-id="10887-522">**NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="10887-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="10887-523">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="10887-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="10887-524">Isso compilará VSTexture, um sombreador de vértice definido anteriormente no arquivo. FX, para o vertex shader versão 1,1 e, em seguida, definirá esse sombreador compilado como o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="10887-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="10887-525">O sombreador de pixel é atribuído a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="10887-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="10887-526">Estados de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="10887-526">Shader Constant States</span></span>

<span data-ttu-id="10887-527">Os Estados de constante do sombreador são usados para acessar parâmetros de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="10887-527">Shader constant states are used to access shader constant parameters.</span></span>



| <span data-ttu-id="10887-528">Estado de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="10887-528">Shader Constant State</span></span> | <span data-ttu-id="10887-529">Type</span><span class="sxs-lookup"><span data-stu-id="10887-529">Type</span></span>            | <span data-ttu-id="10887-530">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-530">Values</span></span>                                       |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="10887-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="10887-531">PixelShaderConstant</span></span>   | <span data-ttu-id="10887-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="10887-533">matriz m x n de floats; m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="10887-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="10887-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="10887-535">float4</span><span class="sxs-lookup"><span data-stu-id="10887-535">float4</span></span>          | <span data-ttu-id="10887-536">Um 4D flutuante.</span><span class="sxs-lookup"><span data-stu-id="10887-536">One 4D float.</span></span>                                |
| <span data-ttu-id="10887-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="10887-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="10887-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="10887-538">float4x2</span></span>        | <span data-ttu-id="10887-539">Dois 4D flutuantes.</span><span class="sxs-lookup"><span data-stu-id="10887-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="10887-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="10887-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="10887-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="10887-541">float4x3</span></span>        | <span data-ttu-id="10887-542">Três o 4D floats.</span><span class="sxs-lookup"><span data-stu-id="10887-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="10887-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="10887-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="10887-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="10887-544">float4x4</span></span>        | <span data-ttu-id="10887-545">Quatro o 4D flutua.</span><span class="sxs-lookup"><span data-stu-id="10887-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="10887-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="10887-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="10887-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="10887-548">matriz m x n de BOOLs; m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="10887-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="10887-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="10887-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="10887-551">matriz m x n de ints.</span><span class="sxs-lookup"><span data-stu-id="10887-551">m x n array of ints.</span></span> <span data-ttu-id="10887-552">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-552">m and n are optional.</span></span>   |
| <span data-ttu-id="10887-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="10887-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="10887-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="10887-555">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-555">m x n array of floats.</span></span> <span data-ttu-id="10887-556">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-556">m and n are optional.</span></span> |
| <span data-ttu-id="10887-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="10887-557">VertexShaderConstant</span></span>  | <span data-ttu-id="10887-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="10887-559">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-559">m x n array of floats.</span></span> <span data-ttu-id="10887-560">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-560">m and n are optional.</span></span> |
| <span data-ttu-id="10887-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="10887-561">VertexShaderConstant1</span></span> | <span data-ttu-id="10887-562">float4</span><span class="sxs-lookup"><span data-stu-id="10887-562">float4</span></span>          | <span data-ttu-id="10887-563">Um 4D flutuante.</span><span class="sxs-lookup"><span data-stu-id="10887-563">One 4D float.</span></span>                                |
| <span data-ttu-id="10887-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="10887-564">VertexShaderConstant2</span></span> | <span data-ttu-id="10887-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="10887-565">float4x2</span></span>        | <span data-ttu-id="10887-566">Dois 4D flutuantes.</span><span class="sxs-lookup"><span data-stu-id="10887-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="10887-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="10887-567">VertexShaderConstant3</span></span> | <span data-ttu-id="10887-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="10887-568">float4x3</span></span>        | <span data-ttu-id="10887-569">Três o 4D floats.</span><span class="sxs-lookup"><span data-stu-id="10887-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="10887-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="10887-570">VertexShaderConstant4</span></span> | <span data-ttu-id="10887-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="10887-571">float4x4</span></span>        | <span data-ttu-id="10887-572">Quatro o 4D flutua.</span><span class="sxs-lookup"><span data-stu-id="10887-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="10887-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="10887-573">VertexShaderConstantB</span></span> | <span data-ttu-id="10887-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="10887-575">matriz m x n de BOOLs.</span><span class="sxs-lookup"><span data-stu-id="10887-575">m x n array of bools.</span></span> <span data-ttu-id="10887-576">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-576">m and n are optional.</span></span>  |
| <span data-ttu-id="10887-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="10887-577">VertexShaderConstantI</span></span> | <span data-ttu-id="10887-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="10887-579">matriz m x n de ints.</span><span class="sxs-lookup"><span data-stu-id="10887-579">m x n array of ints.</span></span> <span data-ttu-id="10887-580">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-580">m and n are optional.</span></span>   |
| <span data-ttu-id="10887-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="10887-581">VertexShaderConstantF</span></span> | <span data-ttu-id="10887-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="10887-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="10887-583">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-583">m x n array of floats.</span></span> <span data-ttu-id="10887-584">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="10887-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="10887-585">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="10887-585">Texture States</span></span>

<span data-ttu-id="10887-586">Os Estados de textura inicializam texturas usadas pelo misturador multitextura.</span><span class="sxs-lookup"><span data-stu-id="10887-586">Texture states initialize textures used by the multitexture blender.</span></span>



| <span data-ttu-id="10887-587">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="10887-587">Texture State</span></span> | <span data-ttu-id="10887-588">Type</span><span class="sxs-lookup"><span data-stu-id="10887-588">Type</span></span>    | <span data-ttu-id="10887-589">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-589">Values</span></span>                            |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="10887-590">Textura \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-590">Texture\[8\]</span></span>  | <span data-ttu-id="10887-591">textura</span><span class="sxs-lookup"><span data-stu-id="10887-591">texture</span></span> | <span data-ttu-id="10887-592">**NULL** ou um parâmetro de textura.</span><span class="sxs-lookup"><span data-stu-id="10887-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="10887-593">Estados de estágio de textura</span><span class="sxs-lookup"><span data-stu-id="10887-593">Texture Stage States</span></span>

<span data-ttu-id="10887-594">Estados de estágio de textura configuram texturas e os estágios de textura no misturador multitextura.</span><span class="sxs-lookup"><span data-stu-id="10887-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



| <span data-ttu-id="10887-595">Estado do estágio de textura</span><span class="sxs-lookup"><span data-stu-id="10887-595">Texture Stage State</span></span>        | <span data-ttu-id="10887-596">Type</span><span class="sxs-lookup"><span data-stu-id="10887-596">Type</span></span>  | <span data-ttu-id="10887-597">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-597">Values</span></span>                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10887-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="10887-599">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-599">dword</span></span> | <span data-ttu-id="10887-600">O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="10887-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="10887-601">Consulte D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="10887-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="10887-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="10887-603">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-603">dword</span></span> | <span data-ttu-id="10887-604">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-605">Consulte D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="10887-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="10887-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="10887-607">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-607">dword</span></span> | <span data-ttu-id="10887-608">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-609">Consulte D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="10887-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="10887-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="10887-611">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-611">dword</span></span> | <span data-ttu-id="10887-612">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-613">Consulte D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="10887-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="10887-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="10887-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-615">dword</span></span> | <span data-ttu-id="10887-616">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-617">Consulte D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="10887-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="10887-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="10887-619">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-619">dword</span></span> | <span data-ttu-id="10887-620">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-621">Consulte D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="10887-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="10887-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="10887-623">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-623">dword</span></span> | <span data-ttu-id="10887-624">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-625">Consulte D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="10887-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="10887-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="10887-627">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-627">dword</span></span> | <span data-ttu-id="10887-628">O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="10887-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="10887-629">Consulte D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="10887-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="10887-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="10887-631">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-631">float</span></span> | <span data-ttu-id="10887-632">Os mesmos valores que D3DTSS \_ BUMPENVLSCALE sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="10887-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="10887-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="10887-634">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-634">float</span></span> | <span data-ttu-id="10887-635">Os mesmos valores que D3DTSS \_ BUMPENVLOFFSET sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="10887-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="10887-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="10887-637">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-637">float</span></span> | <span data-ttu-id="10887-638">Mesmos valores que D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="10887-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="10887-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="10887-640">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-640">float</span></span> | <span data-ttu-id="10887-641">Mesmos valores que D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="10887-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="10887-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="10887-643">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-643">float</span></span> | <span data-ttu-id="10887-644">Mesmos valores que D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="10887-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="10887-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="10887-646">FLOAT</span><span class="sxs-lookup"><span data-stu-id="10887-646">float</span></span> | <span data-ttu-id="10887-647">Mesmos valores que D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="10887-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="10887-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="10887-649">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-649">dword</span></span> | <span data-ttu-id="10887-650">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="10887-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="10887-651">Consulte D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="10887-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="10887-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="10887-653">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-653">dword</span></span> | <span data-ttu-id="10887-654">Os mesmos valores que D3DTSS \_ TEXCOORDINDEX sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="10887-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="10887-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="10887-656">DWORD</span><span class="sxs-lookup"><span data-stu-id="10887-656">dword</span></span> | <span data-ttu-id="10887-657">Mesmos valores que [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) valores sem o \_ prefixo D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="10887-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="10887-658">Consulte D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="10887-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="10887-659">Estados de transformação</span><span class="sxs-lookup"><span data-stu-id="10887-659">Transform States</span></span>

<span data-ttu-id="10887-660">Defina Estados de transformação para inicializar matrizes de transformação.</span><span class="sxs-lookup"><span data-stu-id="10887-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="10887-661">Os efeitos usam matrizes transpostas para obter eficiência.</span><span class="sxs-lookup"><span data-stu-id="10887-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="10887-662">Você pode fornecer matrizes transpostas a um efeito, ou um efeito irá transpor automaticamente as matrizes antes de usá-las.</span><span class="sxs-lookup"><span data-stu-id="10887-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



| <span data-ttu-id="10887-663">Estado de transformação</span><span class="sxs-lookup"><span data-stu-id="10887-663">Transform State</span></span>       | <span data-ttu-id="10887-664">Type</span><span class="sxs-lookup"><span data-stu-id="10887-664">Type</span></span>     | <span data-ttu-id="10887-665">Valores</span><span class="sxs-lookup"><span data-stu-id="10887-665">Values</span></span>                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10887-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="10887-666">ProjectionTransform</span></span>   | <span data-ttu-id="10887-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="10887-667">float4x4</span></span> | <span data-ttu-id="10887-668">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="10887-669">Mesmos valores que D3DTS \_ projeção sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="10887-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="10887-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="10887-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="10887-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="10887-671">float4x4</span></span> | <span data-ttu-id="10887-672">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="10887-673">Mesmos valores que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="10887-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="10887-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="10887-674">ViewTransform</span></span>         | <span data-ttu-id="10887-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="10887-675">float4x4</span></span> | <span data-ttu-id="10887-676">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="10887-677">Mesmos valores que D3DTS \_ exibição sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="10887-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="10887-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="10887-678">WorldTransform</span></span>        | <span data-ttu-id="10887-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="10887-679">float4x4</span></span> | <span data-ttu-id="10887-680">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="10887-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="10887-681">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10887-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10887-682">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="10887-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
