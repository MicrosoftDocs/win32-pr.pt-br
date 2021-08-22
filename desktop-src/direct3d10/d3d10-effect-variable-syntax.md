---
description: Uma variável de efeito é declarada com a sintaxe a seguir.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintaxe de variável de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2422ba2cebf18c72a14d621ef13a98700aefd2858169c6e96566b455ec21d2ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497706"
---
# <a name="effect-variable-syntax-direct3d-10"></a>Sintaxe de variável de efeito (Direct3D 10)

Uma variável de efeito é declarada com a sintaxe a seguir.

## <a name="syntax"></a>Syntax

*DataType* *VariableName* \[ : *semanticName* \]  <  *annotations* >;



| Nome         | Descrição                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de dados     | Qualquer [tipo básico](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) ou de [textura.](../direct3dhlsl/dx-graphics-hlsl-to-type.md)                                                                        |
| VariableName | Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de efeito.                                                                                                                   |
| SemanticName | Uma cadeia de caracteres ASCII que denota informações adicionais sobre como uma variável deve ser usada. Uma semântica é uma cadeia de caracteres ASCII que pode ser um valor do sistema predefinido ou uma cadeia de caracteres de usuário personalizado. |
| Anotações  | Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para sintaxe, consulte [Sintaxe de anotação (Direct3D 10)](d3d10-effect-annotation-syntax.md).     |



 

Uma variável de efeito declarada fora de todas as funções é considerada global no escopo; as variáveis declaradas dentro de uma função são locais para essa função.

## <a name="example"></a>Exemplo

O [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variáveis globais sem semântica para cores de material, propriedades de luz e matrizes de transformação.

Este exemplo ilustra as variáveis de efeito global.


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



A amostragem de uma textura é feita com um exemplo de textura. Para configurar um exemplo em um efeito, consulte o [tipo de amostra](../direct3dhlsl/dx-graphics-hlsl-sampler.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](d3d10-effect-format.md)
</dt> </dl>

 

 
