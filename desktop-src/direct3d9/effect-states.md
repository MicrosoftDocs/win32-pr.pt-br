---
description: Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314759"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="bd127-103">Estados de efeito (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bd127-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="bd127-104">Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.</span><span class="sxs-lookup"><span data-stu-id="bd127-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="bd127-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="bd127-105">Where:</span></span>

-   <span data-ttu-id="bd127-106">Estado de efeito – semelhante aos Estados de pipeline de função fixa tradicional.</span><span class="sxs-lookup"><span data-stu-id="bd127-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="bd127-107">Uma lista completa de Estados é fornecida abaixo.</span><span class="sxs-lookup"><span data-stu-id="bd127-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="bd127-108">\[\[ \] índice \] do -Índice inteiro opcional.</span><span class="sxs-lookup"><span data-stu-id="bd127-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="bd127-109">O índice identifica um estado específico dentro de uma matriz de Estados de efeito.</span><span class="sxs-lookup"><span data-stu-id="bd127-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="bd127-110">Os colchetes externos indicam que um índice é opcional.</span><span class="sxs-lookup"><span data-stu-id="bd127-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="bd127-111">Se um índice for usado, certifique-se de usar os colchetes internos.</span><span class="sxs-lookup"><span data-stu-id="bd127-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="bd127-112">Expression – expressão de atribuição de estado.</span><span class="sxs-lookup"><span data-stu-id="bd127-112">expression - State assignment expression.</span></span> <span data-ttu-id="bd127-113">Consulte [Expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="bd127-114">Cada Estado tem um tipo de dados nativo.</span><span class="sxs-lookup"><span data-stu-id="bd127-114">Each state has a native data type.</span></span> <span data-ttu-id="bd127-115">Esse é o tipo de dados em que o estado espera que os valores estejam quando o efeito os atribui.</span><span class="sxs-lookup"><span data-stu-id="bd127-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="bd127-116">Os tipos de dados esperados por cada Estado estão listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="bd127-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="bd127-117">Observe que a interface de efeito tentará converter valores para o tipo apropriado o mais cedo possível.</span><span class="sxs-lookup"><span data-stu-id="bd127-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="bd127-118">Valores literais podem ser convertidos em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="bd127-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="bd127-119">Não literais (ou seja, variáveis regulares) precisam ser convertidas quando os métodos definidos apropriados são chamados.</span><span class="sxs-lookup"><span data-stu-id="bd127-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="bd127-120">Por exemplo, a interface de efeito converterá valores definidos usando [**setbool**](id3dxbaseeffect--setbool.md), [**DefinirValor**](id3dxbaseeffect--setvalue.md)e outras funções semelhantes, se necessário.</span><span class="sxs-lookup"><span data-stu-id="bd127-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="bd127-121">Para melhorar o desempenho, verifique se os valores passados para a interface de efeito já são do tipo correto e não precisarão de conversão.</span><span class="sxs-lookup"><span data-stu-id="bd127-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="bd127-122">Se o tempo de execução não puder converter um valor, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="bd127-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="bd127-123">Os Estados de efeito podem ser divididos nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="bd127-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="bd127-124">Estados claros</span><span class="sxs-lookup"><span data-stu-id="bd127-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="bd127-125">Estados de material</span><span class="sxs-lookup"><span data-stu-id="bd127-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="bd127-126">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="bd127-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="bd127-127">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="bd127-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="bd127-128">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="bd127-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="bd127-129">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="bd127-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="bd127-130">Estados de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="bd127-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="bd127-131">Estados do sombreador</span><span class="sxs-lookup"><span data-stu-id="bd127-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="bd127-132">Estados de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="bd127-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="bd127-133">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="bd127-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="bd127-134">Estados de estágio de textura</span><span class="sxs-lookup"><span data-stu-id="bd127-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="bd127-135">Estados de transformação</span><span class="sxs-lookup"><span data-stu-id="bd127-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="bd127-136">Estados claros</span><span class="sxs-lookup"><span data-stu-id="bd127-136">Light States</span></span>

<span data-ttu-id="bd127-137">Para habilitar o melhor desempenho para a aplicação de um efeito, todos os componentes de uma luz ou um material devem ser especificados no arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="bd127-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="bd127-138">Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de luz individualmente.</span><span class="sxs-lookup"><span data-stu-id="bd127-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd127-139">Estado claro</span><span class="sxs-lookup"><span data-stu-id="bd127-139">Light State</span></span>            | <span data-ttu-id="bd127-140">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-140">Type</span></span>   | <span data-ttu-id="bd127-141">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="bd127-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="bd127-143">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-143">float4</span></span> | <span data-ttu-id="bd127-144">Consulte o membro de ambiente de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="bd127-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="bd127-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-146">float</span></span>  | <span data-ttu-id="bd127-147">Consulte o membro Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="bd127-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="bd127-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-149">float</span></span>  | <span data-ttu-id="bd127-150">Consulte o membro Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="bd127-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="bd127-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-152">float</span></span>  | <span data-ttu-id="bd127-153">Consulte o membro Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="bd127-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="bd127-155">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-155">float4</span></span> | <span data-ttu-id="bd127-156">Consulte o membro difuso de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="bd127-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="bd127-158">float3</span><span class="sxs-lookup"><span data-stu-id="bd127-158">float3</span></span> | <span data-ttu-id="bd127-159">Consulte o membro de direção de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="bd127-160">N mais claro \[\]</span><span class="sxs-lookup"><span data-stu-id="bd127-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="bd127-161">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-161">bool</span></span>   | <span data-ttu-id="bd127-162">**True** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="bd127-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="bd127-163">Consulte o argumento bEnable em [**clarear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="bd127-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="bd127-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="bd127-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-165">float</span></span>  | <span data-ttu-id="bd127-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="bd127-167">Consulte o membro de queda de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="bd127-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="bd127-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-169">float</span></span>  | <span data-ttu-id="bd127-170">Consulte o membro Phi de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="bd127-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="bd127-172">float3</span><span class="sxs-lookup"><span data-stu-id="bd127-172">float3</span></span> | <span data-ttu-id="bd127-173">Consulte o membro position de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="bd127-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-174">LightRange\[n\]</span></span>        | <span data-ttu-id="bd127-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-175">float</span></span>  | <span data-ttu-id="bd127-176">Consulte o membro Range de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="bd127-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="bd127-178">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-178">float4</span></span> | <span data-ttu-id="bd127-179">Consulte o membro especular de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="bd127-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="bd127-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-181">float</span></span>  | <span data-ttu-id="bd127-182">Consulte o membro teta de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="bd127-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bd127-183">LightType\[n\]</span></span>         | <span data-ttu-id="bd127-184">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-184">dword</span></span>  | <span data-ttu-id="bd127-185">Mesmo valor que a matriz de até n valores de [**D3DLIGHTTYPE**](./d3dlighttype.md) sem o \_ prefixo D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="bd127-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="bd127-186">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="bd127-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="bd127-187">Isso habilitará a iluminação, tornará a iluminação do tipo, definirá a posição da luz como float3<10.0 f, 1,0 f, 23.0 f> e definirá a cor do ambiente como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1.0>.</span><span class="sxs-lookup"><span data-stu-id="bd127-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="bd127-188">Estados de material</span><span class="sxs-lookup"><span data-stu-id="bd127-188">Material States</span></span>

<span data-ttu-id="bd127-189">Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de material individualmente.</span><span class="sxs-lookup"><span data-stu-id="bd127-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="bd127-190">Estado do material</span><span class="sxs-lookup"><span data-stu-id="bd127-190">Material State</span></span>   | <span data-ttu-id="bd127-191">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-191">Type</span></span>   | <span data-ttu-id="bd127-192">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-192">Values</span></span>                                         |
| <span data-ttu-id="bd127-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="bd127-193">MaterialAmbient</span></span>  | <span data-ttu-id="bd127-194">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-194">float4</span></span> | <span data-ttu-id="bd127-195">Mesmo valor que o [ **ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bd127-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="bd127-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="bd127-196">MaterialDiffuse</span></span>  | <span data-ttu-id="bd127-197">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-197">float4</span></span> | <span data-ttu-id="bd127-198">Mesmo valor que [ **difusa**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bd127-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="bd127-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="bd127-199">MaterialEmissive</span></span> | <span data-ttu-id="bd127-200">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-200">float4</span></span> | <span data-ttu-id="bd127-201">Mesmo valor que [ **emissiva**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bd127-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="bd127-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="bd127-202">MaterialPower</span></span>    | <span data-ttu-id="bd127-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-203">float</span></span>  | <span data-ttu-id="bd127-204">Mesmo valor que a [ **energia**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bd127-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="bd127-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="bd127-205">MaterialSpecular</span></span> | <span data-ttu-id="bd127-206">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-206">float4</span></span> | <span data-ttu-id="bd127-207">Mesmo valor que [ **especular**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bd127-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="bd127-208">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="bd127-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="bd127-209">Isso definirá a cor difusa como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f> e tornará o poder do material 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="bd127-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="bd127-210">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="bd127-210">Render States</span></span>

<span data-ttu-id="bd127-211">Há dois tipos de Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="bd127-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="bd127-212">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="bd127-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="bd127-213">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="bd127-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="bd127-214">Estados de renderização de pipe de pixel</span><span class="sxs-lookup"><span data-stu-id="bd127-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="bd127-215">Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="bd127-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd127-216">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="bd127-216">Render State</span></span></td>
<td><span data-ttu-id="bd127-217">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-217">Type</span></span></td>
<td><span data-ttu-id="bd127-218">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="bd127-220">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-220">bool</span></span></td>
<td><span data-ttu-id="bd127-221">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-221">True or False.</span></span> <span data-ttu-id="bd127-222">Os mesmos valores que D3DRS_ALPHABLENDENABLE em <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bd127-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="bd127-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="bd127-224">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-224">dword</span></span></td>
<td><span data-ttu-id="bd127-225">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="bd127-226">Consulte D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="bd127-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="bd127-227">AlphaRef</span></span></td>
<td><span data-ttu-id="bd127-228">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-228">dword</span></span></td>
<td><span data-ttu-id="bd127-229">Mesmos valores que D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="bd127-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="bd127-231">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-231">dword</span></span></td>
<td><span data-ttu-id="bd127-232">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-232">True or False.</span></span> <span data-ttu-id="bd127-233">Consulte D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="bd127-234">BlendOp</span></span></td>
<td><span data-ttu-id="bd127-235">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-235">dword</span></span></td>
<td><span data-ttu-id="bd127-236">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sem o prefixo D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="bd127-238">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-238">dword</span></span></td>
<td><span data-ttu-id="bd127-239">Combinação de bits de vermelho | VERDE | AZUL | Alfa.</span><span class="sxs-lookup"><span data-stu-id="bd127-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="bd127-240">Consulte D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="bd127-241">DepthBias</span></span></td>
<td><span data-ttu-id="bd127-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-242">float</span></span></td>
<td><span data-ttu-id="bd127-243">Mesmos valores que D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="bd127-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="bd127-244">DestBlend</span></span></td>
<td><span data-ttu-id="bd127-245">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-245">dword</span></span></td>
<td><span data-ttu-id="bd127-246">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="bd127-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-247">DitherEnable</span></span></td>
<td><span data-ttu-id="bd127-248">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-248">bool</span></span></td>
<td><span data-ttu-id="bd127-249">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-249">True or False.</span></span> <span data-ttu-id="bd127-250">Mesmos valores que D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="bd127-251">FillMode</span></span></td>
<td><span data-ttu-id="bd127-252">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-252">dword</span></span></td>
<td><span data-ttu-id="bd127-253">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sem o prefixo D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="bd127-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="bd127-254">LastPixel</span></span></td>
<td><span data-ttu-id="bd127-255">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-255">dword</span></span></td>
<td><span data-ttu-id="bd127-256">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-256">True or False.</span></span> <span data-ttu-id="bd127-257">Consulte D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="bd127-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-258">Shadmode</span><span class="sxs-lookup"><span data-stu-id="bd127-258">ShadeMode</span></span></td>
<td><span data-ttu-id="bd127-259">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-259">dword</span></span></td>
<td><span data-ttu-id="bd127-260">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sem o prefixo D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="bd127-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="bd127-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="bd127-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-262">float</span></span></td>
<td><span data-ttu-id="bd127-263">Mesmos valores que D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="bd127-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="bd127-264">SrcBlend</span></span></td>
<td><span data-ttu-id="bd127-265">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-265">dword</span></span></td>
<td><span data-ttu-id="bd127-266">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="bd127-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="bd127-268">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-268">bool</span></span></td>
<td><span data-ttu-id="bd127-269">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-269">True or False.</span></span> <span data-ttu-id="bd127-270">Mesmos valores que D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-271">StencilEnable</span></span></td>
<td><span data-ttu-id="bd127-272">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-272">bool</span></span></td>
<td><span data-ttu-id="bd127-273">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-273">True or False.</span></span> <span data-ttu-id="bd127-274">Mesmos valores que D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="bd127-275">StencilFail</span></span></td>
<td><span data-ttu-id="bd127-276">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-276">dword</span></span></td>
<td><span data-ttu-id="bd127-277">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="bd127-278">Consulte D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="bd127-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="bd127-279">StencilFunc</span></span></td>
<td><span data-ttu-id="bd127-280">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-280">dword</span></span></td>
<td><span data-ttu-id="bd127-281">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="bd127-282">Consulte D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="bd127-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="bd127-283">StencilMask</span></span></td>
<td><span data-ttu-id="bd127-284">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-284">dword</span></span></td>
<td><span data-ttu-id="bd127-285">Mesmos valores que D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="bd127-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="bd127-286">StencilPass</span></span></td>
<td><span data-ttu-id="bd127-287">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-287">dword</span></span></td>
<td><span data-ttu-id="bd127-288">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="bd127-289">Consulte D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="bd127-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="bd127-290">StencilRef</span></span></td>
<td><span data-ttu-id="bd127-291">INT</span><span class="sxs-lookup"><span data-stu-id="bd127-291">int</span></span></td>
<td><span data-ttu-id="bd127-292">Mesmos valores que D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="bd127-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="bd127-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="bd127-294">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-294">dword</span></span></td>
<td><span data-ttu-id="bd127-295">Mesmos valores que D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="bd127-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="bd127-296">StencilZFail</span></span></td>
<td><span data-ttu-id="bd127-297">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-297">dword</span></span></td>
<td><span data-ttu-id="bd127-298">Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="bd127-299">Consulte D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="bd127-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="bd127-300">TextureFactor</span></span></td>
<td><span data-ttu-id="bd127-301">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-301">dword</span></span></td>
<td><span data-ttu-id="bd127-302">Mesmos valores que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bd127-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="bd127-303">Mesmos valores que D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="bd127-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="bd127-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="bd127-305">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-305">dword</span></span></td>
<td><span data-ttu-id="bd127-306">Os valores são os mesmos que os valores usados pelo D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="bd127-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="bd127-307">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="bd127-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="bd127-308">COORD0 (que corresponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="bd127-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="bd127-309">COORD1 (que corresponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="bd127-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="bd127-310">COORD2 (que corresponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="bd127-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="bd127-311">COORD3 (que corresponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="bd127-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="bd127-312">U (que corresponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="bd127-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="bd127-313">V (que corresponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="bd127-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="bd127-314">W (que corresponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="bd127-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-315">ZEnable</span></span></td>
<td><span data-ttu-id="bd127-316">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-316">dword</span></span></td>
<td><span data-ttu-id="bd127-317">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sem o prefixo D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="bd127-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd127-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="bd127-318">ZFunc</span></span></td>
<td><span data-ttu-id="bd127-319">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-319">dword</span></span></td>
<td><span data-ttu-id="bd127-320">Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="bd127-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="bd127-321">Consulte D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="bd127-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd127-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="bd127-323">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-323">bool</span></span></td>
<td><span data-ttu-id="bd127-324">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-324">True or False.</span></span> <span data-ttu-id="bd127-325">Consulte D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bd127-326">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="bd127-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="bd127-327">Isso habilitará a mistura alfa e fará com que todas as geometrias sejam renderizadas em wireframe.</span><span class="sxs-lookup"><span data-stu-id="bd127-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="bd127-328">Estados de renderização de pipe de vértice</span><span class="sxs-lookup"><span data-stu-id="bd127-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="bd127-329">Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.</span><span class="sxs-lookup"><span data-stu-id="bd127-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd127-330">Estado de renderização</span><span class="sxs-lookup"><span data-stu-id="bd127-330">Render State</span></span>             | <span data-ttu-id="bd127-331">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-331">Type</span></span>   | <span data-ttu-id="bd127-332">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-332">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="bd127-333">Ambiente</span><span class="sxs-lookup"><span data-stu-id="bd127-333">Ambient</span></span>                  | <span data-ttu-id="bd127-334">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-334">float4</span></span> | <span data-ttu-id="bd127-335">Mesmos valores que D3DRS \_ ambiente.</span><span class="sxs-lookup"><span data-stu-id="bd127-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="bd127-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bd127-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="bd127-337">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-337">dword</span></span>  | <span data-ttu-id="bd127-338">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bd127-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bd127-339">Consulte D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bd127-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="bd127-340">Recortando</span><span class="sxs-lookup"><span data-stu-id="bd127-340">Clipping</span></span>                 | <span data-ttu-id="bd127-341">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-341">bool</span></span>   | <span data-ttu-id="bd127-342">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-342">True or False.</span></span> <span data-ttu-id="bd127-343">Mesmos valores que o \_ recorte de D3DRS.</span><span class="sxs-lookup"><span data-stu-id="bd127-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="bd127-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="bd127-345">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-345">dword</span></span>  | <span data-ttu-id="bd127-346">Combinação de bits de D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="bd127-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="bd127-347">Consulte [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="bd127-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="bd127-348">ColorVertex</span></span>              | <span data-ttu-id="bd127-349">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-349">bool</span></span>   | <span data-ttu-id="bd127-350">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-350">True or False.</span></span> <span data-ttu-id="bd127-351">Mesmos valores que D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="bd127-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="bd127-352">De seleção</span><span class="sxs-lookup"><span data-stu-id="bd127-352">CullMode</span></span>                 | <span data-ttu-id="bd127-353">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-353">dword</span></span>  | <span data-ttu-id="bd127-354">Mesmos valores que [**D3DCULL**](./d3dcull.md) sem o \_ prefixo D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="bd127-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="bd127-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bd127-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="bd127-356">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-356">dword</span></span>  | <span data-ttu-id="bd127-357">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bd127-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bd127-358">Consulte D3DRS \_ DiffuseMaterialSource.</span><span class="sxs-lookup"><span data-stu-id="bd127-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="bd127-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bd127-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="bd127-360">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-360">dword</span></span>  | <span data-ttu-id="bd127-361">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bd127-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bd127-362">Consulte D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bd127-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="bd127-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="bd127-363">FogColor</span></span>                 | <span data-ttu-id="bd127-364">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-364">dword</span></span>  | <span data-ttu-id="bd127-365">Mesmos valores que [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="bd127-366">Consulte D3DRS \_ FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="bd127-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="bd127-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="bd127-367">FogDensity</span></span>               | <span data-ttu-id="bd127-368">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-368">float</span></span>  | <span data-ttu-id="bd127-369">Mesmos valores que D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="bd127-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="bd127-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-370">FogEnable</span></span>                | <span data-ttu-id="bd127-371">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-371">bool</span></span>   | <span data-ttu-id="bd127-372">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-372">True or False.</span></span> <span data-ttu-id="bd127-373">Mesmos valores que D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="bd127-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="bd127-374">FogEnd</span></span>                   | <span data-ttu-id="bd127-375">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-375">float</span></span>  | <span data-ttu-id="bd127-376">Mesmos valores que D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="bd127-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="bd127-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="bd127-377">FogStart</span></span>                 | <span data-ttu-id="bd127-378">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-378">float</span></span>  | <span data-ttu-id="bd127-379">Mesmos valores que D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="bd127-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="bd127-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="bd127-380">FogTableMode</span></span>             | <span data-ttu-id="bd127-381">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-381">dword</span></span>  | <span data-ttu-id="bd127-382">Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="bd127-383">Consulte D3DRS \_ FOGTABLEMODE no [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="bd127-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="bd127-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="bd127-384">FogVertexMode</span></span>            | <span data-ttu-id="bd127-385">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-385">dword</span></span>  | <span data-ttu-id="bd127-386">Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md) sem o \_ prefixo D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="bd127-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="bd127-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="bd127-388">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-388">bool</span></span>   | <span data-ttu-id="bd127-389">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-389">True or False.</span></span> <span data-ttu-id="bd127-390">Mesmos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="bd127-391">Iluminação</span><span class="sxs-lookup"><span data-stu-id="bd127-391">Lighting</span></span>                 | <span data-ttu-id="bd127-392">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-392">bool</span></span>   | <span data-ttu-id="bd127-393">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-393">True or False.</span></span> <span data-ttu-id="bd127-394">Mesmos valores que a \_ iluminação D3DRS.</span><span class="sxs-lookup"><span data-stu-id="bd127-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="bd127-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="bd127-395">LocalViewer</span></span>              | <span data-ttu-id="bd127-396">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-396">bool</span></span>   | <span data-ttu-id="bd127-397">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-397">True or False.</span></span> <span data-ttu-id="bd127-398">Mesmos valores que D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="bd127-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="bd127-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="bd127-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="bd127-400">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-400">bool</span></span>   | <span data-ttu-id="bd127-401">Mesmos valores que D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="bd127-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="bd127-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="bd127-402">MultiSampleMask</span></span>          | <span data-ttu-id="bd127-403">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-403">dword</span></span>  | <span data-ttu-id="bd127-404">Mesmos valores que D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="bd127-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="bd127-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="bd127-405">NormalizeNormals</span></span>         | <span data-ttu-id="bd127-406">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-406">bool</span></span>   | <span data-ttu-id="bd127-407">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-407">True or False.</span></span> <span data-ttu-id="bd127-408">Mesmos valores que D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="bd127-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="bd127-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="bd127-409">PatchSegments</span></span>            | <span data-ttu-id="bd127-410">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-410">float</span></span>  | <span data-ttu-id="bd127-411">Mesmos valores que nSegments em [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="bd127-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="bd127-412">PointScale \_ A</span><span class="sxs-lookup"><span data-stu-id="bd127-412">PointScale\_A</span></span>            | <span data-ttu-id="bd127-413">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-413">float</span></span>  | <span data-ttu-id="bd127-414">Os mesmos valores que D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="bd127-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="bd127-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="bd127-415">PointScale\_B</span></span>            | <span data-ttu-id="bd127-416">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-416">float</span></span>  | <span data-ttu-id="bd127-417">Os mesmos valores que D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="bd127-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="bd127-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="bd127-418">PointScale\_C</span></span>            | <span data-ttu-id="bd127-419">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-419">float</span></span>  | <span data-ttu-id="bd127-420">Os mesmos valores que D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="bd127-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="bd127-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-421">PointScaleEnable</span></span>         | <span data-ttu-id="bd127-422">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-422">bool</span></span>   | <span data-ttu-id="bd127-423">Mesmos valores que D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="bd127-424">Pontos</span><span class="sxs-lookup"><span data-stu-id="bd127-424">PointSize</span></span>                | <span data-ttu-id="bd127-425">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-425">float</span></span>  | <span data-ttu-id="bd127-426">Os mesmos valores que D3DRS \_ apontam.</span><span class="sxs-lookup"><span data-stu-id="bd127-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="bd127-427">Pontos \_ mínimos</span><span class="sxs-lookup"><span data-stu-id="bd127-427">PointSize\_Min</span></span>           | <span data-ttu-id="bd127-428">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-428">float</span></span>  | <span data-ttu-id="bd127-429">Os mesmos valores que D3DRS \_ apontam \_ mín.</span><span class="sxs-lookup"><span data-stu-id="bd127-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="bd127-430">Pontos \_ máximos</span><span class="sxs-lookup"><span data-stu-id="bd127-430">PointSize\_Max</span></span>           | <span data-ttu-id="bd127-431">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-431">float</span></span>  | <span data-ttu-id="bd127-432">Os mesmos valores que D3DRS \_ aponta para \_ Max sem o \_ prefixo D3DRS.</span><span class="sxs-lookup"><span data-stu-id="bd127-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="bd127-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-433">PointSpriteEnable</span></span>        | <span data-ttu-id="bd127-434">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-434">bool</span></span>   | <span data-ttu-id="bd127-435">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-435">True or False.</span></span> <span data-ttu-id="bd127-436">Mesmos valores que D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="bd127-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-437">RangeFogEnable</span></span>           | <span data-ttu-id="bd127-438">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-438">bool</span></span>   | <span data-ttu-id="bd127-439">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-439">True or False.</span></span> <span data-ttu-id="bd127-440">Mesmos valores que D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="bd127-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="bd127-441">SpecularEnable</span></span>           | <span data-ttu-id="bd127-442">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-442">bool</span></span>   | <span data-ttu-id="bd127-443">Verdadeiro ou falso.</span><span class="sxs-lookup"><span data-stu-id="bd127-443">True or False.</span></span> <span data-ttu-id="bd127-444">Mesmos valores que D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="bd127-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="bd127-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bd127-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="bd127-446">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-446">dword</span></span>  | <span data-ttu-id="bd127-447">Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bd127-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bd127-448">Consulte D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bd127-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="bd127-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="bd127-449">TweenFactor</span></span>              | <span data-ttu-id="bd127-450">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-450">float</span></span>  | <span data-ttu-id="bd127-451">Mesmos valores que D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="bd127-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="bd127-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="bd127-452">VertexBlend</span></span>              | <span data-ttu-id="bd127-453">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-453">dword</span></span>  | <span data-ttu-id="bd127-454">Mesmos valores que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sem o \_ prefixo D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="bd127-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="bd127-455">Consulte D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="bd127-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="bd127-456">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="bd127-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="bd127-457">Isso fará com que a cor do ambiente FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f>, defina o modo de remoção do backface como contador no sentido anti-horário e defina a cor da neblina como vermelha.</span><span class="sxs-lookup"><span data-stu-id="bd127-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="bd127-458">Estados de amostra</span><span class="sxs-lookup"><span data-stu-id="bd127-458">Sampler States</span></span>

<span data-ttu-id="bd127-459">Um estado de amostra representa um objeto de amostra.</span><span class="sxs-lookup"><span data-stu-id="bd127-459">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="bd127-460">Estado</span><span class="sxs-lookup"><span data-stu-id="bd127-460">State</span></span>   | <span data-ttu-id="bd127-461">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-461">Type</span></span>    | <span data-ttu-id="bd127-462">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-462">Values</span></span>                              |
| <span data-ttu-id="bd127-463">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bd127-463">Sampler</span></span> | <span data-ttu-id="bd127-464">cores</span><span class="sxs-lookup"><span data-stu-id="bd127-464">sampler</span></span> | <span data-ttu-id="bd127-465">**NULL** ou um bloco de estado de amostra.</span><span class="sxs-lookup"><span data-stu-id="bd127-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="bd127-466">Estados de estágio de amostra</span><span class="sxs-lookup"><span data-stu-id="bd127-466">Sampler Stage States</span></span>

<span data-ttu-id="bd127-467">Os Estados de estágio de amostra são usados para amostras de texturas.</span><span class="sxs-lookup"><span data-stu-id="bd127-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="bd127-468">O estado de amostra determina os tipos de filtragem e os modos de endereçamento de textura.</span><span class="sxs-lookup"><span data-stu-id="bd127-468">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd127-469">Estado do classificador</span><span class="sxs-lookup"><span data-stu-id="bd127-469">Sampler State</span></span>       | <span data-ttu-id="bd127-470">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-470">Type</span></span>                         | <span data-ttu-id="bd127-471">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-471">Values</span></span>                                                                                                                            |
| <span data-ttu-id="bd127-472">Endereço de \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-472">AddressU\[16\]</span></span>      | <span data-ttu-id="bd127-473">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-473">dword</span></span>                        | <span data-ttu-id="bd127-474">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="bd127-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="bd127-475">Consulte D3DSAMP \_ AddressU.</span><span class="sxs-lookup"><span data-stu-id="bd127-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="bd127-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-476">AddressV\[16\]</span></span>      | <span data-ttu-id="bd127-477">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-477">dword</span></span>                        | <span data-ttu-id="bd127-478">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="bd127-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="bd127-479">Consulte D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="bd127-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="bd127-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-480">AddressW\[16\]</span></span>      | <span data-ttu-id="bd127-481">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-481">dword</span></span>                        | <span data-ttu-id="bd127-482">Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="bd127-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="bd127-483">Consulte D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="bd127-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="bd127-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="bd127-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bd127-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="bd127-486">Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="bd127-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="bd127-487">Consulte D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="bd127-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="bd127-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="bd127-489">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-489">dword</span></span>                        | <span data-ttu-id="bd127-490">Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="bd127-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="bd127-491">Consulte D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="bd127-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="bd127-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="bd127-493">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-493">dword</span></span>                        | <span data-ttu-id="bd127-494">Os mesmos valores que D3DSAMP \_ MAXANISOTROPY sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bd127-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="bd127-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="bd127-496">INT</span><span class="sxs-lookup"><span data-stu-id="bd127-496">int</span></span>                          | <span data-ttu-id="bd127-497">Os mesmos valores que D3DSAMP \_ MAXMIPLEVEL sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bd127-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="bd127-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="bd127-499">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-499">dword</span></span>                        | <span data-ttu-id="bd127-500">Os mesmos valores que D3DSAMP \_ MINFILTER sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bd127-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="bd127-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="bd127-502">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-502">dword</span></span>                        | <span data-ttu-id="bd127-503">Os mesmos valores que D3DSAMP \_ MIPFILTER sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bd127-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="bd127-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bd127-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="bd127-505">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-505">float</span></span>                        | <span data-ttu-id="bd127-506">Os mesmos valores que D3DSAMP \_ MIPMAPLODBIAS sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bd127-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="bd127-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="bd127-507">SRGBTexture</span></span>         | <span data-ttu-id="bd127-508">bool</span><span class="sxs-lookup"><span data-stu-id="bd127-508">bool</span></span>                         | <span data-ttu-id="bd127-509">Mesmo valor que D3DSAMP \_ SRGBTEXTURE sem o \_ prefixo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bd127-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="bd127-510">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="bd127-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="bd127-511">Isso coloca UVW valores entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="bd127-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="bd127-512">Estados do sombreador</span><span class="sxs-lookup"><span data-stu-id="bd127-512">Shader States</span></span>

<span data-ttu-id="bd127-513">Há apenas dois Estados de sombreador de efeito: um associado a um objeto de sombreador de vértice e o outro associado a um objeto de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="bd127-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bd127-514">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="bd127-514">Shader State</span></span> | <span data-ttu-id="bd127-515">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-515">Type</span></span>         | <span data-ttu-id="bd127-516">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-516">Values</span></span>                                                                      |
| <span data-ttu-id="bd127-517">PixelShader</span><span class="sxs-lookup"><span data-stu-id="bd127-517">PixelShader</span></span>  | <span data-ttu-id="bd127-518">PixelShader</span><span class="sxs-lookup"><span data-stu-id="bd127-518">pixelshader</span></span>  | <span data-ttu-id="bd127-519">**NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="bd127-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="bd127-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="bd127-520">VertexShader</span></span> | <span data-ttu-id="bd127-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="bd127-521">vertexshader</span></span> | <span data-ttu-id="bd127-522">**NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="bd127-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="bd127-523">Exemplo:</span><span class="sxs-lookup"><span data-stu-id="bd127-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="bd127-524">Isso compilará VSTexture, um sombreador de vértice definido anteriormente no arquivo. FX, para o vertex shader versão 1,1 e, em seguida, definirá esse sombreador compilado como o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="bd127-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="bd127-525">O sombreador de pixel é atribuído a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bd127-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="bd127-526">Estados de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="bd127-526">Shader Constant States</span></span>

<span data-ttu-id="bd127-527">Os Estados de constante do sombreador são usados para acessar parâmetros de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bd127-527">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="bd127-528">Estado de constante do sombreador</span><span class="sxs-lookup"><span data-stu-id="bd127-528">Shader Constant State</span></span> | <span data-ttu-id="bd127-529">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-529">Type</span></span>            | <span data-ttu-id="bd127-530">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-530">Values</span></span>                                       |
| <span data-ttu-id="bd127-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="bd127-531">PixelShaderConstant</span></span>   | <span data-ttu-id="bd127-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="bd127-533">matriz m x n de floats; m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="bd127-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="bd127-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="bd127-535">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-535">float4</span></span>          | <span data-ttu-id="bd127-536">Um 4D flutuante.</span><span class="sxs-lookup"><span data-stu-id="bd127-536">One 4D float.</span></span>                                |
| <span data-ttu-id="bd127-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="bd127-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="bd127-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="bd127-538">float4x2</span></span>        | <span data-ttu-id="bd127-539">Dois 4D flutuantes.</span><span class="sxs-lookup"><span data-stu-id="bd127-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="bd127-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="bd127-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="bd127-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="bd127-541">float4x3</span></span>        | <span data-ttu-id="bd127-542">Três o 4D floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="bd127-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="bd127-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="bd127-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="bd127-544">float4x4</span></span>        | <span data-ttu-id="bd127-545">Quatro o 4D flutua.</span><span class="sxs-lookup"><span data-stu-id="bd127-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="bd127-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="bd127-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="bd127-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="bd127-548">matriz m x n de BOOLs; m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="bd127-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="bd127-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="bd127-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="bd127-551">matriz m x n de ints.</span><span class="sxs-lookup"><span data-stu-id="bd127-551">m x n array of ints.</span></span> <span data-ttu-id="bd127-552">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-552">m and n are optional.</span></span>   |
| <span data-ttu-id="bd127-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="bd127-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="bd127-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="bd127-555">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-555">m x n array of floats.</span></span> <span data-ttu-id="bd127-556">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-556">m and n are optional.</span></span> |
| <span data-ttu-id="bd127-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="bd127-557">VertexShaderConstant</span></span>  | <span data-ttu-id="bd127-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="bd127-559">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-559">m x n array of floats.</span></span> <span data-ttu-id="bd127-560">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-560">m and n are optional.</span></span> |
| <span data-ttu-id="bd127-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="bd127-561">VertexShaderConstant1</span></span> | <span data-ttu-id="bd127-562">float4</span><span class="sxs-lookup"><span data-stu-id="bd127-562">float4</span></span>          | <span data-ttu-id="bd127-563">Um 4D flutuante.</span><span class="sxs-lookup"><span data-stu-id="bd127-563">One 4D float.</span></span>                                |
| <span data-ttu-id="bd127-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="bd127-564">VertexShaderConstant2</span></span> | <span data-ttu-id="bd127-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="bd127-565">float4x2</span></span>        | <span data-ttu-id="bd127-566">Dois 4D flutuantes.</span><span class="sxs-lookup"><span data-stu-id="bd127-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="bd127-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="bd127-567">VertexShaderConstant3</span></span> | <span data-ttu-id="bd127-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="bd127-568">float4x3</span></span>        | <span data-ttu-id="bd127-569">Três o 4D floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="bd127-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="bd127-570">VertexShaderConstant4</span></span> | <span data-ttu-id="bd127-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="bd127-571">float4x4</span></span>        | <span data-ttu-id="bd127-572">Quatro o 4D flutua.</span><span class="sxs-lookup"><span data-stu-id="bd127-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="bd127-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="bd127-573">VertexShaderConstantB</span></span> | <span data-ttu-id="bd127-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="bd127-575">matriz m x n de BOOLs.</span><span class="sxs-lookup"><span data-stu-id="bd127-575">m x n array of bools.</span></span> <span data-ttu-id="bd127-576">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-576">m and n are optional.</span></span>  |
| <span data-ttu-id="bd127-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="bd127-577">VertexShaderConstantI</span></span> | <span data-ttu-id="bd127-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="bd127-579">matriz m x n de ints.</span><span class="sxs-lookup"><span data-stu-id="bd127-579">m x n array of ints.</span></span> <span data-ttu-id="bd127-580">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-580">m and n are optional.</span></span>   |
| <span data-ttu-id="bd127-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="bd127-581">VertexShaderConstantF</span></span> | <span data-ttu-id="bd127-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bd127-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="bd127-583">matriz m x n de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-583">m x n array of floats.</span></span> <span data-ttu-id="bd127-584">m e n são opcionais.</span><span class="sxs-lookup"><span data-stu-id="bd127-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="bd127-585">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="bd127-585">Texture States</span></span>

<span data-ttu-id="bd127-586">Os Estados de textura inicializam texturas usadas pelo misturador multitextura.</span><span class="sxs-lookup"><span data-stu-id="bd127-586">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="bd127-587">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="bd127-587">Texture State</span></span> | <span data-ttu-id="bd127-588">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-588">Type</span></span>    | <span data-ttu-id="bd127-589">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-589">Values</span></span>                            |
| <span data-ttu-id="bd127-590">Textura \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-590">Texture\[8\]</span></span>  | <span data-ttu-id="bd127-591">textura</span><span class="sxs-lookup"><span data-stu-id="bd127-591">texture</span></span> | <span data-ttu-id="bd127-592">**NULL** ou um parâmetro de textura.</span><span class="sxs-lookup"><span data-stu-id="bd127-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="bd127-593">Estados de estágio de textura</span><span class="sxs-lookup"><span data-stu-id="bd127-593">Texture Stage States</span></span>

<span data-ttu-id="bd127-594">Estados de estágio de textura configuram texturas e os estágios de textura no misturador multitextura.</span><span class="sxs-lookup"><span data-stu-id="bd127-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd127-595">Estado do estágio de textura</span><span class="sxs-lookup"><span data-stu-id="bd127-595">Texture Stage State</span></span>        | <span data-ttu-id="bd127-596">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-596">Type</span></span>  | <span data-ttu-id="bd127-597">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-597">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="bd127-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="bd127-599">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-599">dword</span></span> | <span data-ttu-id="bd127-600">O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="bd127-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="bd127-601">Consulte D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="bd127-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="bd127-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="bd127-603">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-603">dword</span></span> | <span data-ttu-id="bd127-604">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-605">Consulte D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="bd127-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="bd127-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="bd127-607">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-607">dword</span></span> | <span data-ttu-id="bd127-608">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-609">Consulte D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="bd127-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="bd127-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="bd127-611">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-611">dword</span></span> | <span data-ttu-id="bd127-612">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-613">Consulte D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="bd127-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="bd127-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="bd127-615">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-615">dword</span></span> | <span data-ttu-id="bd127-616">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-617">Consulte D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="bd127-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="bd127-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="bd127-619">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-619">dword</span></span> | <span data-ttu-id="bd127-620">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-621">Consulte D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="bd127-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="bd127-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="bd127-623">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-623">dword</span></span> | <span data-ttu-id="bd127-624">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-625">Consulte D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="bd127-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="bd127-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="bd127-627">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-627">dword</span></span> | <span data-ttu-id="bd127-628">O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="bd127-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="bd127-629">Consulte D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="bd127-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="bd127-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="bd127-631">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-631">float</span></span> | <span data-ttu-id="bd127-632">Os mesmos valores que D3DTSS \_ BUMPENVLSCALE sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="bd127-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="bd127-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="bd127-634">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-634">float</span></span> | <span data-ttu-id="bd127-635">Os mesmos valores que D3DTSS \_ BUMPENVLOFFSET sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="bd127-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="bd127-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="bd127-637">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-637">float</span></span> | <span data-ttu-id="bd127-638">Mesmos valores que D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="bd127-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="bd127-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="bd127-640">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-640">float</span></span> | <span data-ttu-id="bd127-641">Mesmos valores que D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="bd127-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="bd127-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="bd127-643">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-643">float</span></span> | <span data-ttu-id="bd127-644">Mesmos valores que D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="bd127-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="bd127-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="bd127-646">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bd127-646">float</span></span> | <span data-ttu-id="bd127-647">Mesmos valores que D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="bd127-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="bd127-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="bd127-649">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-649">dword</span></span> | <span data-ttu-id="bd127-650">O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bd127-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bd127-651">Consulte D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="bd127-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="bd127-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="bd127-653">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-653">dword</span></span> | <span data-ttu-id="bd127-654">Os mesmos valores que D3DTSS \_ TEXCOORDINDEX sem o \_ prefixo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="bd127-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="bd127-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="bd127-656">DWORD</span><span class="sxs-lookup"><span data-stu-id="bd127-656">dword</span></span> | <span data-ttu-id="bd127-657">Mesmos valores que [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) valores sem o \_ prefixo D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="bd127-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="bd127-658">Consulte D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="bd127-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="bd127-659">Estados de transformação</span><span class="sxs-lookup"><span data-stu-id="bd127-659">Transform States</span></span>

<span data-ttu-id="bd127-660">Defina Estados de transformação para inicializar matrizes de transformação.</span><span class="sxs-lookup"><span data-stu-id="bd127-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="bd127-661">Os efeitos usam matrizes transpostas para obter eficiência.</span><span class="sxs-lookup"><span data-stu-id="bd127-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="bd127-662">Você pode fornecer matrizes transpostas a um efeito, ou um efeito irá transpor automaticamente as matrizes antes de usá-las.</span><span class="sxs-lookup"><span data-stu-id="bd127-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd127-663">Estado de transformação</span><span class="sxs-lookup"><span data-stu-id="bd127-663">Transform State</span></span>       | <span data-ttu-id="bd127-664">Type</span><span class="sxs-lookup"><span data-stu-id="bd127-664">Type</span></span>     | <span data-ttu-id="bd127-665">Valores</span><span class="sxs-lookup"><span data-stu-id="bd127-665">Values</span></span>                                                                                                                          |
| <span data-ttu-id="bd127-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="bd127-666">ProjectionTransform</span></span>   | <span data-ttu-id="bd127-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="bd127-667">float4x4</span></span> | <span data-ttu-id="bd127-668">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="bd127-669">Mesmos valores que D3DTS \_ projeção sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="bd127-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="bd127-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bd127-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="bd127-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="bd127-671">float4x4</span></span> | <span data-ttu-id="bd127-672">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="bd127-673">Mesmos valores que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="bd127-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="bd127-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="bd127-674">ViewTransform</span></span>         | <span data-ttu-id="bd127-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="bd127-675">float4x4</span></span> | <span data-ttu-id="bd127-676">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="bd127-677">Mesmos valores que D3DTS \_ exibição sem o \_ prefixo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="bd127-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="bd127-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="bd127-678">WorldTransform</span></span>        | <span data-ttu-id="bd127-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="bd127-679">float4x4</span></span> | <span data-ttu-id="bd127-680">Uma matriz 4x4 de floats.</span><span class="sxs-lookup"><span data-stu-id="bd127-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="bd127-681">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd127-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd127-682">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="bd127-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
