---
title: Trabalhar com sombreadores e recursos de sombreador
description: É hora de aprender a trabalhar com sombreadores e recursos de sombreador no desenvolvimento de seu jogo Microsoft DirectX para Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366212"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="90908-103">Trabalhar com sombreadores e recursos de sombreador</span><span class="sxs-lookup"><span data-stu-id="90908-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="90908-104">É hora de aprender a trabalhar com sombreadores e recursos de sombreador no desenvolvimento de seu jogo Microsoft DirectX para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="90908-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="90908-105">Vimos como configurar o dispositivo e os recursos gráficos e, talvez, você até mesmo começou a modificar seu pipeline.</span><span class="sxs-lookup"><span data-stu-id="90908-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="90908-106">Agora, vamos examinar os sombreadores de pixel e Vertex.</span><span class="sxs-lookup"><span data-stu-id="90908-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="90908-107">Se você não estiver familiarizado com as linguagens do sombreador, uma discussão rápida está em ordem.</span><span class="sxs-lookup"><span data-stu-id="90908-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="90908-108">Os sombreadores são programas pequenos e de baixo nível que são compilados e executados em estágios específicos no pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="90908-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="90908-109">Sua especialidade é operações matemáticas de ponto flutuante muito rápidas.</span><span class="sxs-lookup"><span data-stu-id="90908-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="90908-110">Os programas de sombreador mais comuns são:</span><span class="sxs-lookup"><span data-stu-id="90908-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="90908-111">**Sombreador de vértice**— executado para cada vértice em uma cena.</span><span class="sxs-lookup"><span data-stu-id="90908-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="90908-112">Esse sombreador opera em elementos de buffer de vértice fornecidos a ele pelo aplicativo de chamada e resulta minimamente em um vetor de posição de 4 componentes que será rasterizado em uma posição de pixel.</span><span class="sxs-lookup"><span data-stu-id="90908-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="90908-113">**Sombreador de pixel**— executado para cada pixel em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="90908-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="90908-114">Esse sombreador recebe coordenadas rasterizadas de estágios de sombreador anteriores (nos pipelines mais simples, esse seria o sombreador de vértice) e retorna uma cor (ou outro valor de 4 componentes) para essa posição de pixel, que é então gravada em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="90908-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="90908-115">Este exemplo inclui um vértice muito básico e sombreadores de pixel que só desenham geometria e sombreadores mais complexos que adicionam cálculos de iluminação básica.</span><span class="sxs-lookup"><span data-stu-id="90908-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="90908-116">Os programas de sombreador são escritos na linguagem de sombreamento de alto nível da Microsoft (HLSL).</span><span class="sxs-lookup"><span data-stu-id="90908-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="90908-117">A sintaxe HLSL é muito parecida com C, mas sem os ponteiros.</span><span class="sxs-lookup"><span data-stu-id="90908-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="90908-118">Os programas de sombreador devem ser muito compactados e eficientes.</span><span class="sxs-lookup"><span data-stu-id="90908-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="90908-119">Se o sombreador for compilado em muitas instruções, ele não poderá ser executado e um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="90908-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="90908-120">(Observe que o número exato de instruções permitidas faz parte do [nível de recurso do Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span><span class="sxs-lookup"><span data-stu-id="90908-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="90908-121">No Direct3D, os sombreadores não são compilados em tempo de execução; Eles são compilados quando o restante do programa é compilado.</span><span class="sxs-lookup"><span data-stu-id="90908-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="90908-122">Quando você compila seu aplicativo com Microsoft Visual Studio 2013, os arquivos HLSL são compilados em arquivos CSO (. CSO) que seu aplicativo deve carregar e posicionar na memória GPU antes do desenho.</span><span class="sxs-lookup"><span data-stu-id="90908-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="90908-123">Certifique-se de incluir esses arquivos de CSO com seu aplicativo ao empacotá-los; Eles são ativos, assim como malhas e texturas.</span><span class="sxs-lookup"><span data-stu-id="90908-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="90908-124">Entender a semântica do HLSL</span><span class="sxs-lookup"><span data-stu-id="90908-124">Understand HLSL semantics</span></span>

<span data-ttu-id="90908-125">É importante levar alguns instantes para discutir a semântica HLSL antes de continuar, pois elas geralmente são um ponto de confusão para novos desenvolvedores de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="90908-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="90908-126">A semântica HLSL são cadeias de caracteres que identificam um valor passado entre o aplicativo e um programa sombreador.</span><span class="sxs-lookup"><span data-stu-id="90908-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="90908-127">Embora possam ser qualquer uma das várias cadeias de caracteres possíveis, a prática recomendada é usar uma cadeia de caracteres como `POSITION` ou `COLOR` que indique o uso.</span><span class="sxs-lookup"><span data-stu-id="90908-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="90908-128">Você atribui essas semânticas ao construir um buffer constante ou layout de entrada.</span><span class="sxs-lookup"><span data-stu-id="90908-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="90908-129">Você também pode adicionar um número de 0 a 7 à semântica, o que permite usar Registros separados para valores semelhantes.</span><span class="sxs-lookup"><span data-stu-id="90908-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="90908-130">Por exemplo: COLOR0, COLOR1, COLOR2...</span><span class="sxs-lookup"><span data-stu-id="90908-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="90908-131">A semântica que é prefixada com "VA \_ " são semânticas de *valor do sistema* que são gravadas pelo seu programa de sombreador; o jogo em si (em execução na CPU) não pode modificá-las.</span><span class="sxs-lookup"><span data-stu-id="90908-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="90908-132">Normalmente, essas semânticas contêm valores que são entradas ou saídas de outro estágio do sombreador no pipeline de gráficos ou que são gerados inteiramente pela GPU.</span><span class="sxs-lookup"><span data-stu-id="90908-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="90908-133">Além disso, a `SV_` semântica tem comportamentos diferentes quando eles são usados para especificar a entrada ou a saída de um estágio do sombreador.</span><span class="sxs-lookup"><span data-stu-id="90908-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="90908-134">Por exemplo, `SV_POSITION` (saída) contém os dados de vértice transformados durante o estágio do sombreador de vértice e `SV_POSITION` (*entrada*) contém os valores de posição de pixel que foram interpolados pela GPU durante o estágio de rasterização.</span><span class="sxs-lookup"><span data-stu-id="90908-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="90908-135">Aqui estão algumas semânticas HLSL comuns:</span><span class="sxs-lookup"><span data-stu-id="90908-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="90908-136">`POSITION`(*n*) para dados de buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="90908-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="90908-137">`SV_POSITION` fornece uma posição de pixel para o sombreador de pixel e não pode ser escrito por seu jogo.</span><span class="sxs-lookup"><span data-stu-id="90908-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="90908-138">`NORMAL`(*n*) para dados normais fornecidos pelo buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="90908-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="90908-139">`TEXCOORD`(*n*) para dados de coordenadas UV de textura fornecidos para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="90908-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="90908-140">`COLOR`(n) para dados de cor RGBA fornecidos para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="90908-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="90908-141">Observe que ele é tratado de forma idêntica para coordenar dados, incluindo a interpolação do valor durante a rasterização; a semântica simplesmente ajuda a identificar se são dados coloridos.</span><span class="sxs-lookup"><span data-stu-id="90908-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="90908-142">`SV_Target`\[n \] para gravação de um sombreador de pixel em uma textura de destino ou outro buffer de pixel.</span><span class="sxs-lookup"><span data-stu-id="90908-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="90908-143">Veremos alguns exemplos de semântica HLSL à medida que examinamos o exemplo.</span><span class="sxs-lookup"><span data-stu-id="90908-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="90908-144">Ler dos buffers de constantes</span><span class="sxs-lookup"><span data-stu-id="90908-144">Read from the constant buffers</span></span>

<span data-ttu-id="90908-145">Qualquer sombreador pode ler de um buffer constante se esse buffer estiver anexado a seu estágio como um recurso.</span><span class="sxs-lookup"><span data-stu-id="90908-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="90908-146">Neste exemplo, somente o sombreador de vértice recebe um buffer de constante.</span><span class="sxs-lookup"><span data-stu-id="90908-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="90908-147">O buffer de constantes é declarado em dois locais: no código C++ e nos arquivos HLSL correspondentes que o acessarão.</span><span class="sxs-lookup"><span data-stu-id="90908-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="90908-148">Veja como a struct do buffer de constantes é declarada no código C++.</span><span class="sxs-lookup"><span data-stu-id="90908-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="90908-149">Ao declarar a estrutura do buffer constante em seu código C++, verifique se todos os dados estão alinhados corretamente ao longo dos limites de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="90908-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="90908-150">A maneira mais fácil de fazer isso é usar tipos [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , como **XMFLOAT4** ou **XMFLOAT4X4**, como visto no código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="90908-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="90908-151">Você também pode proteger contra buffers desalinhados declarando uma declaração estática:</span><span class="sxs-lookup"><span data-stu-id="90908-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="90908-152">Essa linha de código causará um erro no momento da compilação se **ConstantBufferStruct** não estiver alinhado em 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="90908-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="90908-153">Para obter mais informações sobre alinhamento e empacotamento de buffer constante, consulte [regras de empacotamento para variáveis constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="90908-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="90908-154">Agora, veja como o buffer de constantes é declarado no sombreador de vértice HLSL.</span><span class="sxs-lookup"><span data-stu-id="90908-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="90908-155">Todos os buffers — constante, textura, amostra ou outro — devem ter um registro definido para que a GPU possa acessá-los.</span><span class="sxs-lookup"><span data-stu-id="90908-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="90908-156">Cada estágio do sombreador permite até 15 buffers constantes, e cada buffer pode conter até 4.096 variáveis constantes.</span><span class="sxs-lookup"><span data-stu-id="90908-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="90908-157">A sintaxe de declaração Register-Usage é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="90908-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="90908-158">**b \* \* *\#* : um registro para um buffer constante (** CBuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="90908-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="90908-159">**t \* \* *\#* : um registro para um buffer de textura (** tbuffers \* \*).</span><span class="sxs-lookup"><span data-stu-id="90908-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="90908-160">**s \* \* \#**: um registro para uma amostra.</span><span class="sxs-lookup"><span data-stu-id="90908-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="90908-161">(Um classificador define o comportamento de pesquisa para texels no recurso de textura.)</span><span class="sxs-lookup"><span data-stu-id="90908-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="90908-162">Por exemplo, o HLSL para um sombreador de pixel pode pegar uma textura e uma amostra como entrada com uma declaração como esta.</span><span class="sxs-lookup"><span data-stu-id="90908-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="90908-163">Cabe a você atribuir buffers constantes aos registros — quando você configura o pipeline, anexa um buffer constante ao mesmo slot ao qual você o atribuiu no arquivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="90908-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="90908-164">Por exemplo, no tópico anterior, a chamada para [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica ' 0 ' para o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="90908-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="90908-165">Isso informa ao Direct3D para anexar o recurso de buffer constante para registrar 0, que corresponde à atribuição do buffer a ser **registrada (B0)** no arquivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="90908-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="90908-166">Ler dos buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="90908-166">Read from the vertex buffers</span></span>

<span data-ttu-id="90908-167">O buffer de vértice fornece os dados de triângulo para os objetos de cena ao (s) sombreador (es) de vértice.</span><span class="sxs-lookup"><span data-stu-id="90908-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="90908-168">Assim como ocorre com o buffer de constantes, a estrutura do buffer de vértice é declarada no código C++, usando regras de empacotamento semelhantes.</span><span class="sxs-lookup"><span data-stu-id="90908-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="90908-169">Não há formato padrão para dados de vértice no Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="90908-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="90908-170">Em vez disso, definimos nosso próprio layout de dados de vértice usando um descritor; os campos de dados são definidos usando uma matriz de estruturas [**\_ desc de \_ elemento \_ de entrada D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) .</span><span class="sxs-lookup"><span data-stu-id="90908-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="90908-171">Aqui, mostramos um layout de entrada simples que descreve o mesmo formato de vértice do struct anterior:</span><span class="sxs-lookup"><span data-stu-id="90908-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



<span data-ttu-id="90908-172">Se você adicionar dados ao formato de vértice ao modificar o código de exemplo, certifique-se de atualizar o layout de entrada também, ou o sombreador não será capaz de interpretá-lo.</span><span class="sxs-lookup"><span data-stu-id="90908-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="90908-173">Você pode modificar o layout do vértice da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="90908-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="90908-174">Nesse caso, você modificaria a definição de layout de entrada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="90908-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="90908-175">Cada uma das definições de elemento de layout de entrada é prefixada com uma cadeia de caracteres, como "POSITION" ou "NORMAL", que é a semântica que discutimos anteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="90908-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="90908-176">É como um identificador que ajuda a GPU a identificar esse elemento ao processar o vértice.</span><span class="sxs-lookup"><span data-stu-id="90908-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="90908-177">Escolha nomes comuns e significativos para seus elementos de vértice.</span><span class="sxs-lookup"><span data-stu-id="90908-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="90908-178">Assim como ocorre com o buffer de constantes, o sombreador de vértice tem uma definição de buffer correspondente para elementos de vértice de entrada.</span><span class="sxs-lookup"><span data-stu-id="90908-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="90908-179">(É por isso que fornecemos uma referência ao recurso de sombreador de vértice ao criar o layout de entrada – o Direct3D valida o layout de dados por vértice com a estrutura de entrada do sombreador.) Observe como a semântica corresponde entre a definição de layout de entrada e essa declaração de buffer HLSL.</span><span class="sxs-lookup"><span data-stu-id="90908-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="90908-180">No entanto, `COLOR` tem um "0" acrescentado a ele.</span><span class="sxs-lookup"><span data-stu-id="90908-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="90908-181">Não é necessário adicionar o 0 se você tiver apenas um `COLOR` elemento declarado no layout, mas é uma prática recomendada acrescentá-lo caso você opte por adicionar mais elementos de cor no futuro.</span><span class="sxs-lookup"><span data-stu-id="90908-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="90908-182">Passar dados entre sombreadores</span><span class="sxs-lookup"><span data-stu-id="90908-182">Pass data between shaders</span></span>

<span data-ttu-id="90908-183">Os sombreadores assumem tipos de entrada e retornam tipos de saída de suas funções principais na execução.</span><span class="sxs-lookup"><span data-stu-id="90908-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="90908-184">Para o sombreador de vértice definido na seção anterior, o tipo de entrada era a estrutura de entrada do VS \_ e definimos um layout de entrada correspondente e um struct do C++.</span><span class="sxs-lookup"><span data-stu-id="90908-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="90908-185">Uma matriz dessa estrutura é usada para criar um buffer de vértice no método **CREATECUBE** .</span><span class="sxs-lookup"><span data-stu-id="90908-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="90908-186">O sombreador de vértice retorna uma \_ estrutura de entrada PS, que deve conter minimamente a posição de vértice final de 4 componentes (FLOAT4).</span><span class="sxs-lookup"><span data-stu-id="90908-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="90908-187">Esse valor de posição deve ter a semântica de valor do sistema, `SV_POSITION` , declarado para ela para que a GPU tenha os dados necessários para executar a próxima etapa de desenho.</span><span class="sxs-lookup"><span data-stu-id="90908-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="90908-188">Observe que não há uma correspondência de 1:1 entre a saída do sombreador de vértice e a entrada do sombreador de pixel; o sombreador de vértice retorna uma estrutura para cada vértice que é fornecido, mas o sombreador de pixel é executado uma vez para cada pixel.</span><span class="sxs-lookup"><span data-stu-id="90908-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="90908-189">Isso ocorre porque os dados por vértice passam pela primeira vez pelo estágio de rasterização.</span><span class="sxs-lookup"><span data-stu-id="90908-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="90908-190">Esse estágio decide quais pixels "abrangem" a geometria que você está desenhando, computa dados interpolados por vértice para cada pixel e, em seguida, chama o sombreador de pixel uma vez para cada um desses pixels.</span><span class="sxs-lookup"><span data-stu-id="90908-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="90908-191">A interpolação é o comportamento padrão ao rasterizar valores de saída e é essencial em particular para o processamento correto de dados de vetor de saída (vetores leves, Normals e tangentes por vértice, entre outros).</span><span class="sxs-lookup"><span data-stu-id="90908-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="90908-192">Examinar o sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="90908-192">Review the vertex shader</span></span>

<span data-ttu-id="90908-193">O sombreador de vértice de exemplo é muito simples: Pegue um vértice (posição e cor), transforme a posição de coordenadas de modelo em coordenadas projetadas em perspectiva e retorne-a (juntamente com a cor) para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="90908-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="90908-194">Observe que o valor de cor é interpolado à direita junto com os dados de posição, fornecendo um valor diferente para cada pixel, mesmo que o sombreador de vértice não tenha realizado nenhum cálculo no valor de cor.</span><span class="sxs-lookup"><span data-stu-id="90908-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="90908-195">Um sombreador de vértice mais complexo, como um que configura os vértices de um objeto para sombreamento Phong, pode ser mais parecido com este.</span><span class="sxs-lookup"><span data-stu-id="90908-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="90908-196">Nesse caso, estamos aproveitando o fato de que os vetores e os normais são interpolados para aproximar uma superfície de aparência suave.</span><span class="sxs-lookup"><span data-stu-id="90908-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="90908-197">Examinar o sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="90908-197">Review the pixel shader</span></span>

<span data-ttu-id="90908-198">Este sombreador de pixel neste exemplo é bastante possivelmente a quantidade mínima absoluta de código que você pode ter em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="90908-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="90908-199">Ele usa os dados de cores de pixel interpolados gerados durante a rasterização e retorna-os como saída, onde serão gravados em um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="90908-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="90908-200">Quão entediante!</span><span class="sxs-lookup"><span data-stu-id="90908-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="90908-201">A parte importante é a `SV_TARGET` semântica de valor do sistema no valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="90908-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="90908-202">Ele indica que a saída deve ser gravada no destino de renderização primário, que é o buffer de textura fornecido para a cadeia de permuta para exibição.</span><span class="sxs-lookup"><span data-stu-id="90908-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="90908-203">Isso é necessário para sombreadores de pixel-sem os dados de cor do sombreador de pixel, o Direct3D não teria nada para ser exibido!</span><span class="sxs-lookup"><span data-stu-id="90908-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="90908-204">Um exemplo de um sombreador de pixel mais complexo para executar o sombreamento Phong pode ser semelhante a este.</span><span class="sxs-lookup"><span data-stu-id="90908-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="90908-205">Como os vetores e os normais foram interpolados, não precisamos calculá-los por pixel.</span><span class="sxs-lookup"><span data-stu-id="90908-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="90908-206">No entanto, precisamos renormalize-los devido a como funciona a interpolação; Conceitualmente, precisamos "girar" gradualmente o vetor a partir da direção no vértice A até a direção no vértice B, mantendo seu comprimento — a interpolação wheras, em vez disso, corta uma linha reta entre os dois pontos de extremidade de vetor.</span><span class="sxs-lookup"><span data-stu-id="90908-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="90908-207">Em outro exemplo, o sombreador de pixel usa seus próprios buffers de constante que contêm informações de luz e material.</span><span class="sxs-lookup"><span data-stu-id="90908-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="90908-208">O layout de entrada no sombreador de vértice seria expandido para incluir dados normais, e a saída do sombreador de vértice deve incluir vetores transformados para o vértice, a luz e o vértice normal no sistema de coordenadas de exibição.</span><span class="sxs-lookup"><span data-stu-id="90908-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="90908-209">Se você tiver buffers de textura e amostras com registros atribuídos (**t** e **s**, respectivamente), poderá acessá-los no sombreador de pixel também.</span><span class="sxs-lookup"><span data-stu-id="90908-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="90908-210">Os sombreadores são ferramentas muito poderosas que podem ser usadas para gerar recursos de procedimentos como mapas de sombra ou texturas de ruído.</span><span class="sxs-lookup"><span data-stu-id="90908-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="90908-211">Na verdade, as técnicas avançadas exigem que você considere as texturas de forma mais abstrata, não como elementos visuais, mas como buffers.</span><span class="sxs-lookup"><span data-stu-id="90908-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="90908-212">Eles contêm dados como informações de altura ou outros dados que podem ser amostrados no sombreador de pixel final aprovado ou nesse quadro específico como parte de uma passagem de efeitos de vários estágios.</span><span class="sxs-lookup"><span data-stu-id="90908-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="90908-213">Várias amostras é uma ferramenta poderosa e o backbone de muitos efeitos visuais modernos.</span><span class="sxs-lookup"><span data-stu-id="90908-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="90908-214">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="90908-214">Next steps</span></span>

<span data-ttu-id="90908-215">Espero que você esteja familiarizado com o DirectX 11at esse ponto e esteja pronto para começar a trabalhar em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="90908-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="90908-216">Aqui estão alguns links para ajudar a responder a outras perguntas que você pode ter sobre desenvolvimento com DirectX e C++:</span><span class="sxs-lookup"><span data-stu-id="90908-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="90908-217">[Desenvolvendo jogos](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="90908-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="90908-218">[Usar as ferramentas do Visual Studio para programação de jogos DirectX](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="90908-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="90908-219">[Desenvolvimento de jogos DirectX e demonstrativos de exemplo](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="90908-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="90908-220">[Recursos de programação de jogos adicionais](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="90908-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="90908-221">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90908-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90908-222">Trabalhar com recursos do dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="90908-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="90908-223">Entender o pipeline de renderização do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="90908-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 