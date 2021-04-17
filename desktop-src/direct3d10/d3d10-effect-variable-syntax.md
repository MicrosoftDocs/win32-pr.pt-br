---
description: Uma variável de efeito é declarada com a sintaxe a seguir.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintaxe variável de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370441"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Sintaxe variável de efeito (Direct3D 10)

Uma variável de efeito é declarada com a sintaxe a seguir.

## <a name="syntax"></a>Syntax

*DataType* *VariableName* \[ : as anotações *semânticaname* \]  <   >;



| Nome         | Descrição                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de dados     | Qualquer tipo [básico](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) ou de [textura](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .                                                                        |
| VariableName | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de efeito.                                                                                                                   |
| Semânticaname | Uma cadeia de caracteres ASCII que denota informações adicionais sobre como uma variável deve ser usada. Uma semântica é uma cadeia de caracteres ASCII que pode ser um valor de sistema predefinido ou uma cadeia de caracteres de usuário personalizado. |
| Anotações  | Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para obter a sintaxe, consulte [sintaxe de anotação (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Uma variável de efeito que é declarada fora de todas as funções, é considerada global no escopo; variáveis declaradas em uma função são locais para essa função.

## <a name="example"></a>Exemplo

O [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variáveis globais sem semântica para cores de material, Propriedades claras e matrizes de transformação.

Este exemplo ilustra as variáveis de efeito globais.


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



Este exemplo ilustra a declaração de uma variável de textura.


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



A amostragem de uma textura é feita com uma amostra de textura. Para configurar uma amostra em um efeito, consulte o [tipo de amostra](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](d3d10-effect-format.md)
</dt> </dl>

 

 
