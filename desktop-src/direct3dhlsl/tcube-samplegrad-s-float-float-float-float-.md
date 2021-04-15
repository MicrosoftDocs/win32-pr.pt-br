---
title: 'Função SampleGrad:: SampleGrad (S, float, float, float, float) para TextureCube'
description: Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. Para TextureCube
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104506550"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a>Função SampleGrad:: SampleGrad (S, float, float, float, float) para TextureCube

Exemplifica uma textura, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
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

[Métodos SampleGrad](texturecube-samplegrad.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
