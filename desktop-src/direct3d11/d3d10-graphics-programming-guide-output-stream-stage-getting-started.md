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
# <a name="getting-started-with-the-stream-output-stage"></a>Introdução com o estágio de Stream-Output

Esta seção descreve como usar um sombreador de geometria com o estágio de saída de fluxo.

## <a name="compile-a-geometry-shader"></a>Compilar um sombreador de geometria

Este sombreador de geometria (GS) calcula uma face normal para cada triângulo e gera dados de coordenadas de posição, normal e de textura.


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



Tendo esse código em mente, considere que um sombreador de geometria é muito parecido com um vértice ou sombreador de pixel, mas com as seguintes exceções: o tipo retornado pela função, as declarações de parâmetro de entrada e a função intrínseca.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Tipo de retorno da função<br/></td>
<td>O tipo de retorno da função faz uma coisa, declara o número máximo de vértices que podem ser gerados pelo sombreador. Nesse caso, <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

define a saída como um máximo de 12 vértices.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Declarações de parâmetro de entrada</p></td>
<td><p>Essa função usa dois parâmetros de entrada:</p>
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
<p>O primeiro parâmetro é uma matriz de vértices (3, neste caso) definida por uma estrutura de GSPS_INPUT (que define os dados por vértice como uma posição, uma coordenada normal e uma textura). O primeiro parâmetro também usa a palavra-chave triângulo, o que significa que o estágio do assembler de entrada deve gerar dados de saída para o sombreador de geometria como um dos tipos primitivos de triângulo (lista de triângulo ou faixa de triângulo).</p>
<p>O segundo parâmetro é um fluxo de triângulo definido pelo tipo TriangleStream &lt; GSPS_INPUTT &gt; . Isso significa que o parâmetro é uma matriz de triângulos, cada um dos quais é composto de três vértices (que contêm os dados dos membros de GSPS_INPUT).</p>
<p>Use as palavras-chave triângulo e trianglestream para identificar triângulos individuais ou um fluxo de triângulos em um GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Função intrínseca</p></td>
<td><p>As linhas de código na função Shader usam funções intrínsecas Common-shader-Core HLSL, exceto as duas últimas linhas, que chamam Append e RestartStrip. Essas funções só estão disponíveis para um sombreador Geometry. Append informa o sombreador Geometry para acrescentar a saída à faixa atual; RestartStrip cria uma nova faixa primitiva. Uma nova faixa é criada implicitamente em cada invocação do estágio GS.</p></td>
</tr>
</tbody>
</table>



 

O restante do sombreador é muito semelhante a um vértice ou sombreador de pixel. O sombreador de geometria usa uma estrutura para declarar parâmetros de entrada e marca o membro de posição com a semântica de posição da VA \_ para informar ao hardware que esses dados são posicionais. A estrutura de entrada identifica os outros dois parâmetros de entrada como coordenadas de textura (embora um deles contenha uma face normal). Você pode usar sua própria semântica personalizada para a face normal se preferir.

Tendo criado o sombreador Geometry, chame [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) para compilar, conforme mostrado no exemplo de código a seguir.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Assim como os sombreadores de vértices e de pixel, você precisa de um sinalizador de sombreador para informar ao compilador como você deseja que o sombreador seja compilado (para depuração, otimizado para velocidade e assim por diante), a função de ponto de entrada e o modelo de sombreador para validar. Este exemplo cria um sombreador de geometria criado com base no arquivo Tutorial13. FX, usando a função GS. O sombreador é compilado para o modelo de sombreador 4,0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Criar um objeto de Geometry-Shader com saída de fluxo

Depois que você souber que transmitirá os dados da geometria e tiver compilado com êxito o sombreador, a próxima etapa será chamar [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) para criar o objeto Geometry Shader.

Mas primeiro, é necessário declarar a assinatura de entrada do terreno (saída de fluxo). Essa assinatura corresponde ou valida as saídas GS e as entradas de saída no momento da criação do objeto. O código a seguir é um exemplo da declaração de is.


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



Essa função usa vários parâmetros, incluindo:

-   Um ponteiro para o sombreador de geometria compilado (ou sombreador de vértice se nenhum sombreador de geometria estará presente e os dados serão transmitidos diretamente do sombreador de vértice). Para obter informações sobre como obter esse ponteiro, consulte [obtendo um ponteiro para um sombreador compilado](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Um ponteiro para uma matriz de declarações que descrevem os dados de entrada para o estágio de saída do fluxo. (Consulte [**D3D11 \_ para obter a \_ \_ entrada da declaração**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Você pode fornecer até 64 declarações, uma para cada tipo diferente de elemento a ser impresso no estágio de saída. A matriz de entradas de declaração descreve o layout de dados, independentemente de um único buffer ou de vários buffers serem associados para saída de fluxo.
-   O número de elementos que são gravados pelo estágio de saída.
-   Um ponteiro para o objeto do sombreador Geometry que é criado (consulte [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

Nessa situação, o stride do buffer é nulo, o índice do fluxo a ser enviado ao rasterizador é 0 e a interface de vinculação de classe é nula.

A declaração de saída de fluxo define a maneira como os dados são gravados em um recurso de buffer. Você pode adicionar quantos componentes desejar à declaração de saída. Use o estágio de SO para gravar em um único recurso de buffer ou em muitos recursos de buffer. Para um único buffer, o estágio de SO pode escrever muitos elementos diferentes por vértice. Para vários buffers, o estágio de SO só pode gravar um único elemento de dados por vértice em cada buffer.

Para usar o estágio de SO sem usar um sombreador de geometria, chame [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) e passe um ponteiro para um sombreador de vértice para o parâmetro *pShaderBytecode* .

## <a name="set-the-output-targets"></a>Definir os destinos de saída

A última etapa é definir os buffers de estágio de SO. Os dados podem ser transmitidos em um ou mais buffers na memória para uso posterior. O código a seguir mostra como criar um único buffer que pode ser usado para dados de vértice, bem como para o estágio de teste para transmitir dados para o.


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



Crie um buffer chamando [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). Este exemplo ilustra o uso padrão, que é típico para um recurso de buffer que deve ser atualizado com muita frequência pela CPU. O sinalizador de associação identifica o estágio de pipeline ao qual o recurso pode ser associado. Qualquer recurso usado pelo estágio de saída também deve ser criado com o sinalizador de associação D3D10 de \_ entrada do fluxo de associação \_ \_ .

Depois que o buffer for criado com êxito, defina-o para o dispositivo atual chamando [**ID3D11DeviceContext:: SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Essa chamada usa o número de buffers, um ponteiro para os buffers e uma matriz de deslocamentos (um deslocamento em cada um dos buffers que indica onde começar a gravar dados). Os dados serão gravados nesses buffers de saída de streaming quando uma função de desenho for chamada. Uma variável interna controla a posição de onde começar a gravar dados nos buffers de saída de streaming e que as variáveis continuarão a ser incrementadas até que [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) seja chamado novamente e um novo valor de deslocamento seja especificado.

Todos os dados gravados nos buffers de destino serão valores de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fluxo-estágio de saída](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

