---
title: Sintaxe de variável de efeito (Direct3D 11)
description: Uma variável de efeito é declarada com a sintaxe descrita nesta seção.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25057f3cd2535a0b48072616c3dd59393f90a24fe044c1cdad8acea677a541ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538389"
---
# <a name="effect-variable-syntax-direct3d-11"></a>Sintaxe de variável de efeito (Direct3D 11)

Uma variável de efeito é declarada com a sintaxe descrita nesta seção.

## <a name="syntax"></a>Sintaxe

Sintaxe básica:

*DataType* *VariableName* \[ *: semânticoname* \]  <  *anotações*  >  \[ = inicialvalue \] ;

Consulte [sintaxe de variável (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) para obter a sintaxe completa.



| Name         | Descrição                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de dados     | Qualquer modo de exibição de acesso, sombreador ou tipo de bloco [básico](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), de [textura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)e não ordenado.                            |
| VariableName | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de efeito.                                                                                                                   |
| Semânticaname | Uma cadeia de caracteres ASCII que denota informações adicionais sobre como uma variável deve ser usada. Uma semântica é uma cadeia de caracteres ASCII que pode ser um valor de sistema predefinido ou uma cadeia de caracteres de usuário personalizado. |
| Anotações  | Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para obter a sintaxe, consulte [sintaxe de anotação (Direct3D 11)](d3d11-effect-annotation-syntax.md).     |
| Inicialvalue | O valor padrão da variável.                                                                                                                                                          |



 

Uma variável de efeito que é declarada fora de todas as funções, é considerada global no escopo; variáveis declaradas em uma função são locais para essa função.

## <a name="example"></a>Exemplo

Este exemplo ilustra as variáveis numéricas de efeito global.


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



Este exemplo ilustra as variáveis de efeito que são locais para uma função de sombreador.


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



Este exemplo ilustra os parâmetros de função que têm semântica.


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



Este exemplo ilustra a declaração de uma variável de textura global.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



A amostragem de uma textura é feita com uma amostra de textura. Para configurar uma amostra em um efeito, consulte o [tipo de amostra](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).

Este exemplo ilustra a declaração de variáveis de exibição de acesso não ordenado globais.


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](d3d11-effect-format.md)
</dt> </dl>

 

 