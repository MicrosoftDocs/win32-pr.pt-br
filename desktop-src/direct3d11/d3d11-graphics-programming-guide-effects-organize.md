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
# <a name="organizing-state-in-an-effect-direct3d-11"></a>Organizando o estado em um efeito (Direct3D 11)

Com o Direct3D 11, o estado do efeito para determinados estágios de pipeline é organizado por estruturas. Aqui estão as estruturas:



| Estado do pipeline | Estrutura                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------|
| Rasterização  | [**D3D11 do \_ rasterizador \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)                                                           |
| Fusão de saída  | [**D3D11 \_ JUNÇÃO \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) DESC e [ **\_ estêncil de profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) |
| Sombreadores        | Veja abaixo                                                                                                          |



 

Para os estágios do sombreador, em que o número de alterações de estado precisa ser mais controlado por um aplicativo, o estado foi dividido em estado de buffer constante, estado de amostra, estado de recurso do sombreador e estado de exibição de acesso não ordenado (para sombreadores de pixel e computação). Isso permite que um aplicativo cuidadosamente projetado para atualizar apenas o estado que está mudando, o que melhora o desempenho, reduzindo a quantidade de dados que precisam ser passados para a GPU.

Então, como organizar o estado do pipeline em um efeito?

A resposta é, a ordem não importa. As variáveis globais não precisam estar localizadas na parte superior. No entanto, todos os exemplos no SDK seguem a mesma ordem, pois é uma prática recomendada organizar os dados da mesma maneira. Esta é uma breve descrição da ordenação de dados nos exemplos do SDK do DirectX.

-   [Variáveis globais](#global-variables)
-   [Sombreadores](#shaders)
-   [Grupos, técnicas e passagens](#groups-techniques-and-passes)

## <a name="global-variables"></a>Variáveis globais

Assim como a prática C padrão, as variáveis globais são declaradas primeiro, na parte superior do arquivo. Geralmente, essas são variáveis que serão inicializadas por um aplicativo e, em seguida, usadas em um efeito. Às vezes, eles são inicializados e nunca alterados, outras vezes eles são atualizados a cada quadro. Assim como as regras de escopo da função C, as variáveis de efeito declaradas fora do escopo das funções de efeito são visíveis em todo o efeito; qualquer variável declarada dentro de uma função de efeito só é visível dentro dessa função.

Aqui está um exemplo das variáveis declaradas em BasicHLSL10. FX.


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



A sintaxe das variáveis de efeito é mais totalmente detalhada na [sintaxe variável de efeito (Direct3D 11)](d3d11-effect-variable-syntax.md). A sintaxe de amostragens de textura de efeito é mais detalhada no [tipo de amostra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

## <a name="shaders"></a>Sombreadores

Os sombreadores são pequenos programas executáveis. Você pode considerar os sombreadores como o estado do sombreador de encapsulamento, já que o código HLSL implementa a funcionalidade do sombreador. O pipeline de gráficos de até cinco tipos diferentes de sombreadores.

-   Sombreadores de vértice-operam em dados de vértice. Um vértice no produz um vértice de saída.
-   Sombreadores envoltória – opere nos dados de patch. Fase de ponto de controle: uma invocação produz um ponto de controle; Para cada fase de bifurcação e junção: um patch produz alguma quantidade de dados constantes de patch.
-   Sombreadores de domínio – operam em dados primitivos. Um primitivo pode resultar em 0, 1 ou muitos primitivos de saída.
-   Sombreadores de geometria – opere em dados primitivos. Um primitivo em pode resultar em 0, 1 ou muitos primitivos de saída.
-   Sombreadores de pixel – opere em dados de pixel. Um pixel no produz 1 pixel de saída (a menos que o pixel seja retirado de uma renderização).

O pipeline do sombreador de computação usa um sombreador:

-   Sombreadores de computação – opere em qualquer tipo de dados. A saída é independente do número de threads.

Os sombreadores são funções locais e seguem as regras de função de estilo C. Quando um efeito é compilado, cada sombreador é compilado e um ponteiro para cada função de sombreador é armazenado internamente. Uma interface ID3D11Effect é retornada quando a compilação é bem-sucedida. Neste ponto, o efeito compilado está em um formato intermediário.

Para obter mais informações sobre os sombreadores compilados, você precisará usar a reflexão do sombreador. Isso é, basicamente, como pedir ao tempo de execução para descompilar os sombreadores e retornar informações para você sobre o código do sombreador.


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



A sintaxe dos sombreadores de efeito é mais totalmente detalhada na [sintaxe de função de efeito (Direct3D 11)](d3d11-effect-function-syntax.md).

## <a name="groups-techniques-and-passes"></a>Grupos, técnicas e passagens

Um grupo é uma coleção de técnicas. Uma técnica é uma coleção de passagens de renderização (deve haver pelo menos uma passagem). Cada passagem de efeito (que é semelhante no escopo a uma única passagem em um loop de processamento) define o estado do sombreador e qualquer outro Estado de pipeline necessário para renderizar a geometria.

Os grupos são opcionais. Há um grupo único sem nome que abrange todas as técnicas globais. Todos os outros grupos devem ser nomeados.

Aqui está um exemplo de uma técnica (que inclui uma passagem) de BasicHLSL10. FX.


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



A sintaxe dos sombreadores de efeito é mais detalhada na [sintaxe técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 