---
title: 'SampleGrad:: SampleGrad (S, float, float, float, int, float) function para Texture2D'
description: Amostras de um Texture2D, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe de exemplo de valores LOD (nível de detalhe) de amostra. Para Texture2D.
ms.assetid: 1216B02A-4F70-4804-9B04-37E83DFC1CE8
keywords:
- HLSL da função SampleGrad
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b309eb9bc0ce7cbd968be81fa05eee91ee577b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104989450"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2d"></a>SampleGrad:: SampleGrad (S, float, float, float, int, float) function para Texture2D

Amostras de um [**Texture2D**](sm5-object-texture2d.md), usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe de exemplo de valores LOD (nível de detalhe) de amostra.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Tipo: **samplestate**

Um [estado de amostra](dx-graphics-hlsl-sampler.md). Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.

</dd> <dt>

*Local* \[ do no\]
</dt> <dd>

Tipo: **float**

As coordenadas de textura. O tipo de argumento é dependente do tipo de objeto Texture.



| Tipo de Texture-Object                    | Tipo de parâmetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Campo DDX* \[ em\]
</dt> <dd>

Tipo: **float**

A taxa de alteração da geometria da superfície na direção x. O tipo de argumento é dependente do tipo de objeto Texture.



| Tipo de Texture-Object                      | Tipo de parâmetro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | sem suporte  |



 

</dd> <dt>

*Ddy* \[ no\]
</dt> <dd>

Tipo: **float**

A taxa de alteração da geometria da superfície na direção y. O tipo de argumento é dependente do tipo de objeto Texture.



| Tipo de Texture-Object                      | Tipo de parâmetro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | sem suporte  |



 

</dd> <dt>

*Deslocamento* \[ no\]
</dt> <dd>

Tipo: **int**

Um deslocamento de coordenadas de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Use um deslocamento somente em um inteiro MipLevel; caso contrário, você poderá obter resultados que não se traduzem bem em hardware. O tipo de argumento é dependente do tipo de objeto Texture. Para obter mais informações, consulte [aplicando deslocamentos de inteiro](dx-graphics-hlsl-to-sample.md).



| Tipo de Texture-Object           | Tipo de parâmetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | Int3           |
| TextureCube, TextureCubeArray | sem suporte  |



 

</dd> <dt>

*Fixe* \[ no\]
</dt> <dd>

Tipo: **float**

Um valor opcional para fixe os valores de LOD de exemplo para. Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos SampleGrad](texture2d-samplegrad.md)
</dt> </dl>

 

 
