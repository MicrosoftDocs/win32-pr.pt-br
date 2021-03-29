---
title: Organizando o estado em um efeito (Direct3D 11)
description: Com o Direct3D 11, o estado do efeito para determinados estágios de pipeline é organizado por estruturas.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a0523dd8abdabde29a5485b8d3b1e6d13b9429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988681"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a><span data-ttu-id="e9208-103">Organizando o estado em um efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e9208-103">Organizing State in an Effect (Direct3D 11)</span></span>

<span data-ttu-id="e9208-104">Com o Direct3D 11, o estado do efeito para determinados estágios de pipeline é organizado por estruturas.</span><span class="sxs-lookup"><span data-stu-id="e9208-104">With Direct3D 11, effect state for certain pipeline stages is organized by structures.</span></span> <span data-ttu-id="e9208-105">Aqui estão as estruturas:</span><span class="sxs-lookup"><span data-stu-id="e9208-105">Here are the structures:</span></span>



| <span data-ttu-id="e9208-106">Estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="e9208-106">Pipeline State</span></span> | <span data-ttu-id="e9208-107">Estrutura</span><span class="sxs-lookup"><span data-stu-id="e9208-107">Structure</span></span>                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9208-108">Rasterização</span><span class="sxs-lookup"><span data-stu-id="e9208-108">Rasterization</span></span>  | [<span data-ttu-id="e9208-109">**D3D11 do \_ rasterizador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="e9208-109">**D3D11\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| <span data-ttu-id="e9208-110">Fusão de saída</span><span class="sxs-lookup"><span data-stu-id="e9208-110">Output Merger</span></span>  | <span data-ttu-id="e9208-111">[**D3D11 \_ JUNÇÃO \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) DESC e [ **\_ estêncil de profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="e9208-111">[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) and [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span> |
| <span data-ttu-id="e9208-112">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="e9208-112">Shaders</span></span>        | <span data-ttu-id="e9208-113">Veja abaixo</span><span class="sxs-lookup"><span data-stu-id="e9208-113">See below</span></span>                                                                                                          |



 

<span data-ttu-id="e9208-114">Para os estágios do sombreador, em que o número de alterações de estado precisa ser mais controlado por um aplicativo, o estado foi dividido em estado de buffer constante, estado de amostra, estado de recurso do sombreador e estado de exibição de acesso não ordenado (para sombreadores de pixel e computação).</span><span class="sxs-lookup"><span data-stu-id="e9208-114">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, shader resource state, and unordered access view state (for pixel and compute shaders).</span></span> <span data-ttu-id="e9208-115">Isso permite que um aplicativo cuidadosamente projetado para atualizar apenas o estado que está mudando, o que melhora o desempenho, reduzindo a quantidade de dados que precisam ser passados para a GPU.</span><span class="sxs-lookup"><span data-stu-id="e9208-115">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="e9208-116">Então, como organizar o estado do pipeline em um efeito?</span><span class="sxs-lookup"><span data-stu-id="e9208-116">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="e9208-117">A resposta é, a ordem não importa.</span><span class="sxs-lookup"><span data-stu-id="e9208-117">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="e9208-118">As variáveis globais não precisam estar localizadas na parte superior.</span><span class="sxs-lookup"><span data-stu-id="e9208-118">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="e9208-119">No entanto, todos os exemplos no SDK seguem a mesma ordem, pois é uma prática recomendada organizar os dados da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="e9208-119">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="e9208-120">Esta é uma breve descrição da ordenação de dados nos exemplos do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="e9208-120">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="e9208-121">Variáveis globais</span><span class="sxs-lookup"><span data-stu-id="e9208-121">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="e9208-122">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="e9208-122">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="e9208-123">Grupos, técnicas e passagens</span><span class="sxs-lookup"><span data-stu-id="e9208-123">Groups, Techniques, and Passes</span></span>](#groups-techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="e9208-124">Variáveis globais</span><span class="sxs-lookup"><span data-stu-id="e9208-124">Global Variables</span></span>

<span data-ttu-id="e9208-125">Assim como a prática C padrão, as variáveis globais são declaradas primeiro, na parte superior do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e9208-125">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="e9208-126">Geralmente, essas são variáveis que serão inicializadas por um aplicativo e, em seguida, usadas em um efeito.</span><span class="sxs-lookup"><span data-stu-id="e9208-126">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="e9208-127">Às vezes, eles são inicializados e nunca alterados, outras vezes eles são atualizados a cada quadro.</span><span class="sxs-lookup"><span data-stu-id="e9208-127">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="e9208-128">Assim como as regras de escopo da função C, as variáveis de efeito declaradas fora do escopo das funções de efeito são visíveis em todo o efeito; qualquer variável declarada dentro de uma função de efeito só é visível dentro dessa função.</span><span class="sxs-lookup"><span data-stu-id="e9208-128">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="e9208-129">Aqui está um exemplo das variáveis declaradas em BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="e9208-129">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix


// Texture samplers
SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};
```



<span data-ttu-id="e9208-130">A sintaxe das variáveis de efeito é mais totalmente detalhada na [sintaxe variável de efeito (Direct3D 11)](d3d11-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e9208-130">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 11)](d3d11-effect-variable-syntax.md).</span></span> <span data-ttu-id="e9208-131">A sintaxe de amostragens de textura de efeito é mais detalhada no [tipo de amostra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="e9208-131">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

## <a name="shaders"></a><span data-ttu-id="e9208-132">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="e9208-132">Shaders</span></span>

<span data-ttu-id="e9208-133">Os sombreadores são pequenos programas executáveis.</span><span class="sxs-lookup"><span data-stu-id="e9208-133">Shaders are small executable programs.</span></span> <span data-ttu-id="e9208-134">Você pode considerar os sombreadores como o estado do sombreador de encapsulamento, já que o código HLSL implementa a funcionalidade do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e9208-134">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="e9208-135">O pipeline de gráficos de até cinco tipos diferentes de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="e9208-135">The graphics pipeline up to five different kinds of shaders.</span></span>

-   <span data-ttu-id="e9208-136">Sombreadores de vértice-operam em dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="e9208-136">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="e9208-137">Um vértice no produz um vértice de saída.</span><span class="sxs-lookup"><span data-stu-id="e9208-137">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="e9208-138">Sombreadores envoltória – opere nos dados de patch.</span><span class="sxs-lookup"><span data-stu-id="e9208-138">Hull shaders - Operate on patch data.</span></span> <span data-ttu-id="e9208-139">Fase de ponto de controle: uma invocação produz um ponto de controle; Para cada fase de bifurcação e junção: um patch produz alguma quantidade de dados constantes de patch.</span><span class="sxs-lookup"><span data-stu-id="e9208-139">Control Point Phase: one invocation yields one control point; For each Fork and Join Phases: one patch yields some amount of patch constant data.</span></span>
-   <span data-ttu-id="e9208-140">Sombreadores de domínio – operam em dados primitivos.</span><span class="sxs-lookup"><span data-stu-id="e9208-140">Domain shaders - Operate on primitive data.</span></span> <span data-ttu-id="e9208-141">Um primitivo pode resultar em 0, 1 ou muitos primitivos de saída.</span><span class="sxs-lookup"><span data-stu-id="e9208-141">One primitive may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="e9208-142">Sombreadores de geometria – opere em dados primitivos.</span><span class="sxs-lookup"><span data-stu-id="e9208-142">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="e9208-143">Um primitivo em pode resultar em 0, 1 ou muitos primitivos de saída.</span><span class="sxs-lookup"><span data-stu-id="e9208-143">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="e9208-144">Sombreadores de pixel – opere em dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="e9208-144">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="e9208-145">Um pixel no produz 1 pixel de saída (a menos que o pixel seja retirado de uma renderização).</span><span class="sxs-lookup"><span data-stu-id="e9208-145">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="e9208-146">O pipeline do sombreador de computação usa um sombreador:</span><span class="sxs-lookup"><span data-stu-id="e9208-146">The compute shader pipeline uses one shader:</span></span>

-   <span data-ttu-id="e9208-147">Sombreadores de computação – opere em qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e9208-147">Compute shaders - Operate on any kind of data.</span></span> <span data-ttu-id="e9208-148">A saída é independente do número de threads.</span><span class="sxs-lookup"><span data-stu-id="e9208-148">The output is independent of the number of threads.</span></span>

<span data-ttu-id="e9208-149">Os sombreadores são funções locais e seguem as regras de função de estilo C.</span><span class="sxs-lookup"><span data-stu-id="e9208-149">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="e9208-150">Quando um efeito é compilado, cada sombreador é compilado e um ponteiro para cada função de sombreador é armazenado internamente.</span><span class="sxs-lookup"><span data-stu-id="e9208-150">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="e9208-151">Uma interface ID3D11Effect é retornada quando a compilação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e9208-151">An ID3D11Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="e9208-152">Neste ponto, o efeito compilado está em um formato intermediário.</span><span class="sxs-lookup"><span data-stu-id="e9208-152">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="e9208-153">Para obter mais informações sobre os sombreadores compilados, você precisará usar a reflexão do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e9208-153">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="e9208-154">Isso é, basicamente, como pedir ao tempo de execução para descompilar os sombreadores e retornar informações para você sobre o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e9208-154">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
 
    ....    
    
    return Output;    
}


struct PS_OUTPUT
{
    float4 RGBColor : SV_Target;  // Pixel color
};

PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    ....

    return Output;
}
```



<span data-ttu-id="e9208-155">A sintaxe dos sombreadores de efeito é mais totalmente detalhada na [sintaxe de função de efeito (Direct3D 11)](d3d11-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e9208-155">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 11)](d3d11-effect-function-syntax.md).</span></span>

## <a name="groups-techniques-and-passes"></a><span data-ttu-id="e9208-156">Grupos, técnicas e passagens</span><span class="sxs-lookup"><span data-stu-id="e9208-156">Groups, Techniques, and Passes</span></span>

<span data-ttu-id="e9208-157">Um grupo é uma coleção de técnicas.</span><span class="sxs-lookup"><span data-stu-id="e9208-157">A group is a collection of techniques.</span></span> <span data-ttu-id="e9208-158">Uma técnica é uma coleção de passagens de renderização (deve haver pelo menos uma passagem).</span><span class="sxs-lookup"><span data-stu-id="e9208-158">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="e9208-159">Cada passagem de efeito (que é semelhante no escopo a uma única passagem em um loop de processamento) define o estado do sombreador e qualquer outro Estado de pipeline necessário para renderizar a geometria.</span><span class="sxs-lookup"><span data-stu-id="e9208-159">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="e9208-160">Os grupos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="e9208-160">Groups are optional.</span></span> <span data-ttu-id="e9208-161">Há um grupo único sem nome que abrange todas as técnicas globais.</span><span class="sxs-lookup"><span data-stu-id="e9208-161">There is a single, unnamed group which encompasses all global techniques.</span></span> <span data-ttu-id="e9208-162">Todos os outros grupos devem ser nomeados.</span><span class="sxs-lookup"><span data-stu-id="e9208-162">All other groups must be named.</span></span>

<span data-ttu-id="e9208-163">Aqui está um exemplo de uma técnica (que inclui uma passagem) de BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="e9208-163">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}

fxgroup g0
{
    technique11 RunComputeShader
    {
        pass P0
        {
            SetComputeShader( CompileShader( cs_5_0, CS() ) );
        }
    }
}

```



<span data-ttu-id="e9208-164">A sintaxe dos sombreadores de efeito é mais detalhada na [sintaxe técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e9208-164">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9208-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9208-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9208-166">Efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e9208-166">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 