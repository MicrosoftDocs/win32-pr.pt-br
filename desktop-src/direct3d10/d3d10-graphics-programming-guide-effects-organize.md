---
description: 'Com o Direct3D 10, o estado do efeito para determinados estágios de pipeline é organizado pelas seguintes estruturas:'
ms.assetid: 674ed278-102c-43da-a6bf-58e084df151e
title: Organizando o estado em um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79cbea90c4d42d0a24ec7e35815616bf6698f72f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089045"
---
# <a name="organizing-state-in-an-effect-direct3d-10"></a><span data-ttu-id="f642b-103">Organizando o estado em um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f642b-103">Organizing State in an Effect (Direct3D 10)</span></span>

<span data-ttu-id="f642b-104">Com o Direct3D 10, o estado do efeito para determinados estágios de pipeline é organizado pelas seguintes estruturas:</span><span class="sxs-lookup"><span data-stu-id="f642b-104">With Direct3D 10, effect state for certain pipeline stages is organized by the following structures:</span></span>



| <span data-ttu-id="f642b-105">Estado do pipeline</span><span class="sxs-lookup"><span data-stu-id="f642b-105">Pipeline State</span></span>  | <span data-ttu-id="f642b-106">Estrutura</span><span class="sxs-lookup"><span data-stu-id="f642b-106">Structure</span></span>                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f642b-107">Assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="f642b-107">Input Assembler</span></span> | [<span data-ttu-id="f642b-108">**\_Elemento de entrada d3d10 \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="f642b-108">**D3D10\_INPUT\_ELEMENT\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| <span data-ttu-id="f642b-109">Rasterização</span><span class="sxs-lookup"><span data-stu-id="f642b-109">Rasterization</span></span>   | [<span data-ttu-id="f642b-110">**D3D10 do \_ rasterizador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="f642b-110">**D3D10\_RASTERIZER\_DESC**</span></span>](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| <span data-ttu-id="f642b-111">Fusão de saída</span><span class="sxs-lookup"><span data-stu-id="f642b-111">Output Merger</span></span>   | <span data-ttu-id="f642b-112">[**D3d10 \_ JUNÇÃO \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) DESC e [ **\_ estêncil de profundidade d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="f642b-112">[**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) and [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |



 

<span data-ttu-id="f642b-113">Para os estágios do sombreador, em que o número de alterações de estado precisa ser mais controlado por um aplicativo, o estado foi dividido em estado de buffer constante, estado de amostra e estado de recurso do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642b-113">For the shader stages, where the number of state changes need to be more controlled by an application, the state has been divided up into constant buffer state, sampler state, and shader resource state.</span></span> <span data-ttu-id="f642b-114">Isso permite que um aplicativo cuidadosamente projetado para atualizar apenas o estado que está mudando, o que melhora o desempenho, reduzindo a quantidade de dados que precisam ser passados para a GPU.</span><span class="sxs-lookup"><span data-stu-id="f642b-114">This allows an application that is carefully designed to update only the state that is changing, which improves performance by reducing the amount of data that needs to be passed to the GPU.</span></span>

<span data-ttu-id="f642b-115">Então, como organizar o estado do pipeline em um efeito?</span><span class="sxs-lookup"><span data-stu-id="f642b-115">So how do you organize the pipeline state in an effect?</span></span>

<span data-ttu-id="f642b-116">A resposta é, a ordem não importa.</span><span class="sxs-lookup"><span data-stu-id="f642b-116">The answer is, the order doesn't matter.</span></span> <span data-ttu-id="f642b-117">As variáveis globais não precisam estar localizadas na parte superior.</span><span class="sxs-lookup"><span data-stu-id="f642b-117">Global variables do not have to be located at the top.</span></span> <span data-ttu-id="f642b-118">No entanto, todos os exemplos no SDK seguem a mesma ordem, pois é uma prática recomendada organizar os dados da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="f642b-118">However, all the samples in the SDK follow the same order, as it is good practice to organize the data the same way.</span></span> <span data-ttu-id="f642b-119">Esta é uma breve descrição da ordenação de dados nos exemplos do SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="f642b-119">So this is a brief description of the data ordering in the DirectX SDK samples.</span></span>

-   [<span data-ttu-id="f642b-120">Variáveis globais</span><span class="sxs-lookup"><span data-stu-id="f642b-120">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="f642b-121">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="f642b-121">Shaders</span></span>](#shaders)
-   [<span data-ttu-id="f642b-122">Técnicas e passagens</span><span class="sxs-lookup"><span data-stu-id="f642b-122">Techniques and Passes</span></span>](#techniques-and-passes)

## <a name="global-variables"></a><span data-ttu-id="f642b-123">Variáveis globais</span><span class="sxs-lookup"><span data-stu-id="f642b-123">Global Variables</span></span>

<span data-ttu-id="f642b-124">Assim como a prática C padrão, as variáveis globais são declaradas primeiro, na parte superior do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f642b-124">Just like standard C practice, global variables are declared first, at the top of the file.</span></span> <span data-ttu-id="f642b-125">Geralmente, essas são variáveis que serão inicializadas por um aplicativo e, em seguida, usadas em um efeito.</span><span class="sxs-lookup"><span data-stu-id="f642b-125">Most often, these are variables that will be initialized by an application, and then used in an effect.</span></span> <span data-ttu-id="f642b-126">Às vezes, eles são inicializados e nunca alterados, outras vezes eles são atualizados a cada quadro.</span><span class="sxs-lookup"><span data-stu-id="f642b-126">Sometimes they are initialized and never changed, other times they are updated every frame.</span></span> <span data-ttu-id="f642b-127">Assim como as regras de escopo da função C, as variáveis de efeito declaradas fora do escopo das funções de efeito são visíveis em todo o efeito; qualquer variável declarada dentro de uma função de efeito só é visível dentro dessa função.</span><span class="sxs-lookup"><span data-stu-id="f642b-127">Just like C function scope rules, effect variables declared outside of the scope of effect functions are visible throughout the effect; any variable declared inside of an effect function is only visible within that function.</span></span>

<span data-ttu-id="f642b-128">Aqui está um exemplo das variáveis declaradas em BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="f642b-128">Here is an example of the variables declared in BasicHLSL10.fx.</span></span>


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



<span data-ttu-id="f642b-129">A sintaxe das variáveis de efeito é mais detalhada na [sintaxe variável de efeito (Direct3D 10)](d3d10-effect-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f642b-129">The syntax for effect variables is more fully detailed in [Effect Variable Syntax (Direct3D 10)](d3d10-effect-variable-syntax.md).</span></span> <span data-ttu-id="f642b-130">A sintaxe de amostragens de textura de efeito é mais detalhada no [tipo de amostra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f642b-130">The syntax for effect texture samplers is more fully detailed in [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="shaders"></a><span data-ttu-id="f642b-131">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="f642b-131">Shaders</span></span>

<span data-ttu-id="f642b-132">Os sombreadores são pequenos programas executáveis.</span><span class="sxs-lookup"><span data-stu-id="f642b-132">Shaders are small executable programs.</span></span> <span data-ttu-id="f642b-133">Você pode considerar os sombreadores como o estado do sombreador de encapsulamento, já que o código HLSL implementa a funcionalidade do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642b-133">You can think of shaders as encapsulating shader state, since the HLSL code implements the shader functionality.</span></span> <span data-ttu-id="f642b-134">O pipeline usa três tipos diferentes de sombreadores.</span><span class="sxs-lookup"><span data-stu-id="f642b-134">The pipeline uses three different kinds of shaders.</span></span>

-   <span data-ttu-id="f642b-135">Sombreadores de vértice-operam em dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="f642b-135">Vertex shaders - Operate on vertex data.</span></span> <span data-ttu-id="f642b-136">Um vértice no produz um vértice de saída.</span><span class="sxs-lookup"><span data-stu-id="f642b-136">One vertex in yields one vertex out.</span></span>
-   <span data-ttu-id="f642b-137">Sombreadores de geometria – opere em dados primitivos.</span><span class="sxs-lookup"><span data-stu-id="f642b-137">Geometry shaders - Operate on primitive data.</span></span> <span data-ttu-id="f642b-138">Um primitivo em pode resultar em 0, 1 ou muitos primitivos de saída.</span><span class="sxs-lookup"><span data-stu-id="f642b-138">One primitive in may yield 0, 1, or many primitives out.</span></span>
-   <span data-ttu-id="f642b-139">Sombreadores de pixel – opere em dados de pixel.</span><span class="sxs-lookup"><span data-stu-id="f642b-139">Pixel shaders - Operate on pixel data.</span></span> <span data-ttu-id="f642b-140">Um pixel no produz 1 pixel de saída (a menos que o pixel seja retirado de uma renderização).</span><span class="sxs-lookup"><span data-stu-id="f642b-140">One pixel in yields 1 pixel out (unless the pixel is culled out of a render).</span></span>

<span data-ttu-id="f642b-141">Os sombreadores são funções locais e seguem as regras de função de estilo C.</span><span class="sxs-lookup"><span data-stu-id="f642b-141">Shaders are local functions and follow C style function rules.</span></span> <span data-ttu-id="f642b-142">Quando um efeito é compilado, cada sombreador é compilado e um ponteiro para cada função de sombreador é armazenado internamente.</span><span class="sxs-lookup"><span data-stu-id="f642b-142">When an effect is compiled, each shader is compiled and a pointer to each shader function is stored internally.</span></span> <span data-ttu-id="f642b-143">Uma interface ID3D10Effect é retornada quando a compilação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f642b-143">An ID3D10Effect interface is returned when compilation is successful.</span></span> <span data-ttu-id="f642b-144">Neste ponto, o efeito compilado está em um formato intermediário.</span><span class="sxs-lookup"><span data-stu-id="f642b-144">At this point the compiled effect is in an intermediate format.</span></span>

<span data-ttu-id="f642b-145">Para obter mais informações sobre os sombreadores compilados, você precisará usar a reflexão do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642b-145">To find out more information about the compiled shaders, you will need to use shader reflection.</span></span> <span data-ttu-id="f642b-146">Isso é, basicamente, como pedir ao tempo de execução para descompilar os sombreadores e retornar informações para você sobre o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f642b-146">This is essentially like asking the runtime to decompile the shaders, and return information back to you about the shader code.</span></span>


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



<span data-ttu-id="f642b-147">A sintaxe dos sombreadores de efeito é mais totalmente detalhada na [sintaxe da função de efeito (Direct3D 10)](d3d10-effect-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f642b-147">The syntax for effect shaders is more fully detailed in [Effect Function Syntax (Direct3D 10)](d3d10-effect-function-syntax.md).</span></span>

## <a name="techniques-and-passes"></a><span data-ttu-id="f642b-148">Técnicas e passagens</span><span class="sxs-lookup"><span data-stu-id="f642b-148">Techniques and Passes</span></span>

<span data-ttu-id="f642b-149">Uma técnica é uma coleção de passagens de renderização (deve haver pelo menos uma passagem).</span><span class="sxs-lookup"><span data-stu-id="f642b-149">A technique is a collection of rendering passes (there must be at least one pass).</span></span> <span data-ttu-id="f642b-150">Cada passagem de efeito (que é semelhante no escopo a uma única passagem em um loop de processamento) define o estado do sombreador e qualquer outro Estado de pipeline necessário para renderizar a geometria.</span><span class="sxs-lookup"><span data-stu-id="f642b-150">Each effect pass (which is similar in scope to a single pass in a render loop) defines the shader state and any other pipeline state necessary to render geometry.</span></span>

<span data-ttu-id="f642b-151">Aqui está um exemplo de uma técnica (que inclui uma passagem) de BasicHLSL10. FX.</span><span class="sxs-lookup"><span data-stu-id="f642b-151">Here is an example of one technique (which includes one pass) from BasicHLSL10.fx.</span></span>


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
```



<span data-ttu-id="f642b-152">A sintaxe dos sombreadores de efeito é mais detalhada na [sintaxe técnica de efeito (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f642b-152">The syntax for effect shaders is more fully detailed in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f642b-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f642b-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f642b-154">Efeitos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f642b-154">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 
