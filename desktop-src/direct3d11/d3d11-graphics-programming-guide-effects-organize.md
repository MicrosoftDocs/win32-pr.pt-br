---
title: Organizando o estado em um efeito (Direct3D 11)
description: Com o Direct3D 11, o estado de efeito para determinados estágios de pipeline é organizado por estruturas.
ms.assetid: e5057f94-69dd-4219-a5f4-569e48502475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d36bf99887e96dc5854778edb24f0ceacbc0cdf5a7994532bc2ebd94137fe8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126090"
---
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organizando o estado em um efeito (Direct3D 11)

Com o Direct3D 11, o estado de efeito para determinados estágios de pipeline é organizado por estruturas. Aqui estão as estruturas:



| Estado do pipeline | Estrutura                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rasterization  | [**D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Fusão de saída  | [**D3D11 \_ \_BLEND DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) e [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Sombreadores        | Veja abaixo                                                                                                          |



 

Para os estágios do sombreador, em que o número de alterações de estado precisa ser mais controlado por um aplicativo, o estado foi dividido em estado de buffer constante, estado do exemplo, estado do recurso do sombreador e estado de exibição de acesso não organizado (para sombreadores de computação e pixel). Isso permite que um aplicativo projetado cuidadosamente atualize apenas o estado que está mudando, o que melhora o desempenho reduzindo a quantidade de dados que precisam ser passados para a GPU.

Então, como organizar o estado do pipeline em um efeito?

A resposta é que o pedido não importa. As variáveis globais não devem estar localizadas na parte superior. No entanto, todos os exemplos no SDK seguem a mesma ordem, pois é uma boa prática organizar os dados da mesma maneira. Portanto, esta é uma breve descrição da ordenação de dados nos exemplos do SDK do DirectX.

-   [Variáveis globais](#global-variables)
-   [Sombreadores](#shaders)
-   [Grupos, técnicas e passagens](#groups-techniques-and-passes)

## <a name="global-variables"></a>Variáveis globais

Assim como a prática C padrão, as variáveis globais são declaradas primeiro, na parte superior do arquivo. Na maioria das vezes, essas são variáveis que serão inicializadas por um aplicativo e, em seguida, usadas em um efeito. Às vezes, eles são inicializados e nunca alterados, outras vezes são atualizados a cada quadro. Assim como as regras de escopo da função C, as variáveis de efeito declaradas fora do escopo de funções de efeito são visíveis em todo o efeito; qualquer variável declarada dentro de uma função de efeito só é visível dentro dessa função.

Aqui está um exemplo das variáveis declaradas em BasicHLSL10.fx.


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



A sintaxe para variáveis de efeito é mais detalhada na [Sintaxe da Variável de Efeito (Direct3D 11)](d3d11-effect-variable-syntax.md). A sintaxe para amostras de textura de efeito é mais detalhada em [Tipo de Amostra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

## <a name="shaders"></a>Sombreadores

Sombreadores são programas executáveis pequenos. Você pode pensar em sombreadores como encapsulando o estado do sombreador, pois o código HLSL implementa a funcionalidade do sombreador. O pipeline de gráficos até cinco tipos diferentes de sombreadores.

-   Sombreadores de vértice – operar em dados de vértice. Um vértice em produz um vértice.
-   Sombreadores de chassi – operar em dados de patch. Fase do Ponto de Controle: uma invocação produz um ponto de controle; Para cada fase de bifurcação e junção: um patch produz alguma quantidade de dados constantes de patch.
-   Sombreadores de domínio – operam em dados primitivos. Um primitivo pode produzir 0, 1 ou muitos primitivos.
-   Sombreadores de geometria – operam em dados primitivos. Um primitivo em pode produzir 0, 1 ou muitos primitivos.
-   Sombreadores de pixel – operar em dados de pixel. Um pixel em produz 1 pixel de saída (a menos que o pixel seja eliminado de uma renderização).

O pipeline do sombreador de computação usa um sombreador:

-   Sombreadores de computação – operam em qualquer tipo de dados. A saída é independente do número de threads.

Sombreadores são funções locais e seguem as regras de função de estilo C. Quando um efeito é compilado, cada sombreador é compilado e um ponteiro para cada função de sombreador é armazenado internamente. Uma interface ID3D11Effect é retornada quando a compilação é bem-sucedida. Neste ponto, o efeito compilado está em um formato intermediário.

Para saber mais sobre os sombreadores compilados, você precisará usar a reflexão do sombreador. Isso é essencialmente como pedir ao runtime para descompilar os sombreadores e retornar informações sobre o código do sombreador.


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



A sintaxe para sombreadores de efeito é mais detalhada na [Sintaxe da Função de Efeito (Direct3D 11)](d3d11-effect-function-syntax.md).

## <a name="groups-techniques-and-passes"></a>Grupos, técnicas e passagens

Um grupo é uma coleção de técnicas. Uma técnica é uma coleção de passagens de renderização (deve haver pelo menos uma passagem). Cada passagem de efeito (que é semelhante no escopo a uma única passagem em um loop de renderização) define o estado do sombreador e qualquer outro estado de pipeline necessário para renderizar a geometria.

Os grupos são opcionais. Há um único grupo sem nome que abrange todas as técnicas globais. Todos os outros grupos devem ser nomeados.

Aqui está um exemplo de uma técnica (que inclui uma passagem) de BasicHLSL10.fx.


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



A sintaxe para sombreadores de efeito é mais detalhada na Sintaxe da Técnica de [Efeito (Direct3D 11)](d3d11-effect-technique-syntax.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 