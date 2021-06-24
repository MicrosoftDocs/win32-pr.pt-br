---
title: Introdução com o estágio de Stream-Output
description: Esta seção descreve como usar um sombreador de geometria com o estágio de saída de fluxo.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2e72d25177926c948f43996b6c57d42a7c557b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587873"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="1a718-103">Introdução com o estágio de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="1a718-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="1a718-104">Esta seção descreve como usar um sombreador de geometria com o estágio de saída de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1a718-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="1a718-105">Compilar um sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="1a718-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="1a718-106">Este sombreador de geometria (GS) calcula uma face normal para cada triângulo e gera dados de coordenadas de posição, normal e de textura.</span><span class="sxs-lookup"><span data-stu-id="1a718-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



<span data-ttu-id="1a718-107">Tendo esse código em mente, considere que um sombreador de geometria é muito parecido com um vértice ou sombreador de pixel, mas com as seguintes exceções: o tipo retornado pela função, as declarações de parâmetro de entrada e a função intrínseca.</span><span class="sxs-lookup"><span data-stu-id="1a718-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a718-108">Item</span><span class="sxs-lookup"><span data-stu-id="1a718-108">Item</span></span></th>
<th><span data-ttu-id="1a718-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a718-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a718-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Tipo de retorno da função</span><span class="sxs-lookup"><span data-stu-id="1a718-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="1a718-111">O tipo de retorno da função faz uma coisa, declara o número máximo de vértices que podem ser gerados pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a718-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="1a718-112">Nesse caso, <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="1a718-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1a718-113">define a saída como um máximo de 12 vértices.</span><span class="sxs-lookup"><span data-stu-id="1a718-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a718-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Declarações de parâmetro de entrada</span><span class="sxs-lookup"><span data-stu-id="1a718-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="1a718-115">Essa função usa dois parâmetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="1a718-115">This function takes two input parameters:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="1a718-116">O primeiro parâmetro é uma matriz de vértices (3, neste caso) definida por uma estrutura de GSPS_INPUT (que define os dados por vértice como uma posição, uma coordenada normal e uma textura).</span><span class="sxs-lookup"><span data-stu-id="1a718-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="1a718-117">O primeiro parâmetro também usa a palavra-chave triângulo, o que significa que o estágio do assembler de entrada deve gerar dados de saída para o sombreador de geometria como um dos tipos primitivos de triângulo (lista de triângulo ou faixa de triângulo).</span><span class="sxs-lookup"><span data-stu-id="1a718-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="1a718-118">O segundo parâmetro é um fluxo de triângulo definido pelo tipo TriangleStream &lt; GSPS_INPUTT &gt; .</span><span class="sxs-lookup"><span data-stu-id="1a718-118">The second parameter is a triangle stream defined by the type TriangleStream&lt;GSPS_INPUTT&gt;.</span></span> <span data-ttu-id="1a718-119">Isso significa que o parâmetro é uma matriz de triângulos, cada um dos quais é composto de três vértices (que contêm os dados dos membros de GSPS_INPUT).</span><span class="sxs-lookup"><span data-stu-id="1a718-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="1a718-120">Use as palavras-chave triângulo e trianglestream para identificar triângulos individuais ou um fluxo de triângulos em um GS.</span><span class="sxs-lookup"><span data-stu-id="1a718-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a718-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Função intrínseca</span><span class="sxs-lookup"><span data-stu-id="1a718-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="1a718-122">As linhas de código na função Shader usam funções intrínsecas Common-shader-Core HLSL, exceto as duas últimas linhas, que chamam Append e RestartStrip.</span><span class="sxs-lookup"><span data-stu-id="1a718-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="1a718-123">Essas funções só estão disponíveis para um sombreador Geometry.</span><span class="sxs-lookup"><span data-stu-id="1a718-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="1a718-124">Append informa o sombreador Geometry para acrescentar a saída à faixa atual; RestartStrip cria uma nova faixa primitiva.</span><span class="sxs-lookup"><span data-stu-id="1a718-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="1a718-125">Uma nova faixa é criada implicitamente em cada invocação do estágio GS.</span><span class="sxs-lookup"><span data-stu-id="1a718-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1a718-126">O restante do sombreador é muito semelhante a um vértice ou sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="1a718-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="1a718-127">O sombreador de geometria usa uma estrutura para declarar parâmetros de entrada e marca o membro de posição com a semântica de posição da VA \_ para informar ao hardware que esses dados são posicionais.</span><span class="sxs-lookup"><span data-stu-id="1a718-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="1a718-128">A estrutura de entrada identifica os outros dois parâmetros de entrada como coordenadas de textura (embora um deles contenha uma face normal).</span><span class="sxs-lookup"><span data-stu-id="1a718-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="1a718-129">Você pode usar sua própria semântica personalizada para a face normal se preferir.</span><span class="sxs-lookup"><span data-stu-id="1a718-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="1a718-130">Tendo criado o sombreador Geometry, chame [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) para compilar, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a718-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="1a718-131">Assim como os sombreadores de vértices e de pixel, você precisa de um sinalizador de sombreador para informar ao compilador como você deseja que o sombreador seja compilado (para depuração, otimizado para velocidade e assim por diante), a função de ponto de entrada e o modelo de sombreador para validar.</span><span class="sxs-lookup"><span data-stu-id="1a718-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="1a718-132">Este exemplo cria um sombreador de geometria criado com base no arquivo Tutorial13. FX, usando a função GS.</span><span class="sxs-lookup"><span data-stu-id="1a718-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="1a718-133">O sombreador é compilado para o modelo de sombreador 4,0.</span><span class="sxs-lookup"><span data-stu-id="1a718-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="1a718-134">Criar um objeto de Geometry-Shader com saída de fluxo</span><span class="sxs-lookup"><span data-stu-id="1a718-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="1a718-135">Depois que você souber que transmitirá os dados da geometria e tiver compilado com êxito o sombreador, a próxima etapa será chamar [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) para criar o objeto Geometry Shader.</span><span class="sxs-lookup"><span data-stu-id="1a718-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="1a718-136">Mas primeiro, é necessário declarar a assinatura de entrada do terreno (saída de fluxo).</span><span class="sxs-lookup"><span data-stu-id="1a718-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="1a718-137">Essa assinatura corresponde ou valida as saídas GS e as entradas de saída no momento da criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="1a718-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="1a718-138">O código a seguir é um exemplo da declaração de is.</span><span class="sxs-lookup"><span data-stu-id="1a718-138">The following code is an example of the SO declaration.</span></span>


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



<span data-ttu-id="1a718-139">Essa função usa vários parâmetros, incluindo:</span><span class="sxs-lookup"><span data-stu-id="1a718-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="1a718-140">Um ponteiro para o sombreador de geometria compilado (ou sombreador de vértice se nenhum sombreador de geometria estará presente e os dados serão transmitidos diretamente do sombreador de vértice).</span><span class="sxs-lookup"><span data-stu-id="1a718-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="1a718-141">Para obter informações sobre como obter esse ponteiro, consulte [obtendo um ponteiro para um sombreador compilado](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span><span class="sxs-lookup"><span data-stu-id="1a718-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="1a718-142">Um ponteiro para uma matriz de declarações que descrevem os dados de entrada para o estágio de saída do fluxo.</span><span class="sxs-lookup"><span data-stu-id="1a718-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="1a718-143">(Consulte [**D3D11 \_ para obter a \_ \_ entrada da declaração**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Você pode fornecer até 64 declarações, uma para cada tipo diferente de elemento a ser impresso no estágio de saída.</span><span class="sxs-lookup"><span data-stu-id="1a718-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="1a718-144">A matriz de entradas de declaração descreve o layout de dados, independentemente de um único buffer ou de vários buffers serem associados para saída de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1a718-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="1a718-145">O número de elementos que são gravados pelo estágio de saída.</span><span class="sxs-lookup"><span data-stu-id="1a718-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="1a718-146">Um ponteiro para o objeto do sombreador Geometry que é criado (consulte [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span><span class="sxs-lookup"><span data-stu-id="1a718-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="1a718-147">Nessa situação, o stride do buffer é nulo, o índice do fluxo a ser enviado ao rasterizador é 0 e a interface de vinculação de classe é nula.</span><span class="sxs-lookup"><span data-stu-id="1a718-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="1a718-148">A declaração de saída de fluxo define a maneira como os dados são gravados em um recurso de buffer.</span><span class="sxs-lookup"><span data-stu-id="1a718-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="1a718-149">Você pode adicionar quantos componentes desejar à declaração de saída.</span><span class="sxs-lookup"><span data-stu-id="1a718-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="1a718-150">Use o estágio de SO para gravar em um único recurso de buffer ou em muitos recursos de buffer.</span><span class="sxs-lookup"><span data-stu-id="1a718-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="1a718-151">Para um único buffer, o estágio de SO pode escrever muitos elementos diferentes por vértice.</span><span class="sxs-lookup"><span data-stu-id="1a718-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="1a718-152">Para vários buffers, o estágio de SO só pode gravar um único elemento de dados por vértice em cada buffer.</span><span class="sxs-lookup"><span data-stu-id="1a718-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="1a718-153">Para usar o estágio de SO sem usar um sombreador de geometria, chame [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) e passe um ponteiro para um sombreador de vértice para o parâmetro *pShaderBytecode* .</span><span class="sxs-lookup"><span data-stu-id="1a718-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="1a718-154">Definir os destinos de saída</span><span class="sxs-lookup"><span data-stu-id="1a718-154">Set the Output Targets</span></span>

<span data-ttu-id="1a718-155">A última etapa é definir os buffers de estágio de SO.</span><span class="sxs-lookup"><span data-stu-id="1a718-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="1a718-156">Os dados podem ser transmitidos em um ou mais buffers na memória para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="1a718-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="1a718-157">O código a seguir mostra como criar um único buffer que pode ser usado para dados de vértice, bem como para o estágio de teste para transmitir dados para o.</span><span class="sxs-lookup"><span data-stu-id="1a718-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



<span data-ttu-id="1a718-158">Crie um buffer chamando [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span><span class="sxs-lookup"><span data-stu-id="1a718-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="1a718-159">Este exemplo ilustra o uso padrão, que é típico para um recurso de buffer que deve ser atualizado com muita frequência pela CPU.</span><span class="sxs-lookup"><span data-stu-id="1a718-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="1a718-160">O sinalizador de associação identifica o estágio de pipeline ao qual o recurso pode ser associado.</span><span class="sxs-lookup"><span data-stu-id="1a718-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="1a718-161">Qualquer recurso usado pelo estágio de saída também deve ser criado com o sinalizador de associação D3D10 de \_ entrada do fluxo de associação \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1a718-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="1a718-162">Depois que o buffer for criado com êxito, defina-o para o dispositivo atual chamando [**ID3D11DeviceContext:: SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="1a718-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="1a718-163">Essa chamada usa o número de buffers, um ponteiro para os buffers e uma matriz de deslocamentos (um deslocamento em cada um dos buffers que indica onde começar a gravar dados).</span><span class="sxs-lookup"><span data-stu-id="1a718-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="1a718-164">Os dados serão gravados nesses buffers de saída de streaming quando uma função de desenho for chamada.</span><span class="sxs-lookup"><span data-stu-id="1a718-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="1a718-165">Uma variável interna controla a posição de onde começar a gravar dados nos buffers de saída de streaming e que as variáveis continuarão a ser incrementadas até que [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) seja chamado novamente e um novo valor de deslocamento seja especificado.</span><span class="sxs-lookup"><span data-stu-id="1a718-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="1a718-166">Todos os dados gravados nos buffers de destino serão valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1a718-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a718-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a718-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a718-168">Fluxo-estágio de saída</span><span class="sxs-lookup"><span data-stu-id="1a718-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

