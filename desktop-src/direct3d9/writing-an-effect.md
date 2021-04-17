---
description: Escrever um efeito requer que você compreenda a sintaxe de efeito e gere as informações de estado necessárias. Você pode adicionar estado do sombreador, textura e estado de amostra e todo o estado do pipeline que seu aplicativo requer em um efeito.
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: Escrevendo um efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0f456c5a2bce66f782b4da7d426de5c86bbb33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105813013"
---
# <a name="writing-an-effect-direct3d-9"></a>Escrevendo um efeito (Direct3D 9)

Escrever um efeito requer que você compreenda a sintaxe de efeito e gere as informações de estado necessárias. Você pode adicionar estado do sombreador, textura e estado de amostra e todo o estado do pipeline que seu aplicativo requer em um efeito.

A sintaxe de efeito é detalhada no [formato de efeito (Direct3D 9)](dx9-graphics-reference-effects-file-format.md). Um efeito é normalmente encapsulado em um arquivo de efeito (. FX), mas também pode ser escrito como uma cadeia de caracteres de texto em um aplicativo.

## <a name="effect-example"></a>Exemplo de efeito

Os efeitos contêm três tipos de Estado: estado do sombreador, estado de textura e amostra e estado do pipeline. Aqui está um exemplo de um efeito do [exemplo de BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

texture g_MeshTexture;              // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
// Texture samplers
sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};
struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
  
    float4 vAnimatedPos = vPos;
    
    // Animation the vertex based on time and the vertex's object space position
    if( bAnimate )
        vAnimatedPos += float4(vNormal, 0) * (sin(g_fTime+5.5)+0.5)*5;
    
    // Transform the position from object space to homogeneous projection space
    Output.Position = mul(vAnimatedPos, g_mWorldViewProjection);
    
    // Transform the normal from object space to world space    
    vNormalWorldSpace = normalize(mul(vNormal, (float3x3)g_mWorld));
    
    // Compute simple directional lighting equation
    float3 vTotalLightDiffuse = float3(0,0,0);
    for(int i=0; i < nNumLights; i++ )
        vTotalLightDiffuse += g_LightDiffuse[i] * max(0,dot(vNormalWorldSpace, g_LightDir[i]));
        
    Output.Diffuse.rgb = g_MaterialDiffuseColor * vTotalLightDiffuse + 
                         g_MaterialAmbientColor * g_LightAmbient;   
    Output.Diffuse.a = 1.0f; 
    
    // Just copy the texture coordinate through
    if( bTexture ) 
        Output.TextureUV = vTexCoord0; 
    else
        Output.TextureUV = 0; 
    
    return Output;    
}
struct PS_OUTPUT
{
    float4 RGBColor : COLOR0;  // Pixel color    
};
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_1_1 RenderScenePS( true ); 
    }
}
```



Esse efeito contém:

-   O estado do sombreador, que é todo o estado associado ao sombreador de vértice e ao sombreador de pixel. Isso é definido pelas funções de vértice e sombreador de pixel, quaisquer variáveis globais necessárias e suas estruturas de dados de entrada e saída, todas listadas aqui:

    ```
    struct VS_OUTPUT
    {  ...  };
    VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                             ...
    {  ...  }

    struct PS_OUTPUT
    {  ...  };
    PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                             uniform bool bTexture ) 
    {  ...  }
    ```

    

-   Estado de textura e amostra, que são as variáveis globais para o objeto de textura e o objeto de amostra:

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   O outro Estado de efeito. Não há nenhum outro Estado de efeito explicitamente usado neste exemplo. Se houvesse, seria a técnica dentro da passagem à qual ela foi aplicada:

    ```
    technique RenderSceneWithTexture1Light
    {
        pass P0
        {          
            // Any other effect state can be set here.

            VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
            PixelShader  = compile ps_1_1 RenderScenePS( true ); 
        }
    }
    
    ```

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a>Os efeitos contêm uma ou mais técnicas e aprovações

As opções de renderização de efeito são controladas pela adição de técnicas e passagens.

Os efeitos podem ser criados com passagens adicionais para facilitar os efeitos de renderização mais complexos. Uma técnica dá suporte a um número arbitrário de passagens:


```
technique T0
{
    pass P0
    { ... }

    pass P1
    { ... }

    ...

    pass Pn
    { ... }
}
```



Os efeitos também podem ser criados com um número arbitrário de técnicas.


```
technique T0
{
    pass P0
    { ... }
}

technique T1
{
    pass P0
    { ... }

    pass P1
    { ... }
}

...

technique Tn
{
    pass P0
    { ... }
}

technique TVertexShaderOnly
{
    pass P0
    {
        VertexShader =
        asm
        {
         // assembly-language shader code goes here
         ...
        };
    }
}
```



As técnicas e as passagens podem receber nomes arbitrários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Effect](effects.md)
</dt> </dl>

 

 



