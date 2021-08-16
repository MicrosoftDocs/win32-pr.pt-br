---
title: Função SampleGrad::SampleGrad(S,float,float,float,int,float,uint) para Texture2D
description: Amostra um Texture2D, usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixar valores lod (nível de detalhes) de exemplo.
ms.assetid: 896497E1-A795-4674-AB41-2440A7D0CC76
keywords:
- Função SampleGrad HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e91f2beebd3fb13dfe9e166056611bf1942c176b9fa537910c64ab9ff71c625f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510474"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2d"></a>Função SampleGrad::SampleGrad(S,float,float,float,int,float,uint) para Texture2D

Amostra um [**Texture2D**](sm5-object-texture2d.md), usando um gradiente para influenciar a maneira como o local de exemplo é calculado, com um valor opcional para fixar valores lod (nível de detalhes) de exemplo. Retorna o status sobre a operação.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Tipo: **SamplerState**

Um [estado sampler](dx-graphics-hlsl-sampler.md). Esse é um objeto declarado em um arquivo de efeito que contém atribuições de estado.

</dd> <dt>

*Localização* \[ Em\]
</dt> <dd>

Tipo: **float**

As coordenadas de textura. O tipo de argumento depende do tipo de objeto de textura.



| Texture-Object tipo                    | Tipo de parâmetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*DDX* \[ em\]
</dt> <dd>

Tipo: **float**

A taxa de alteração da geometria da superfície na direção x. O tipo de argumento depende do tipo de objeto de textura.



| Texture-Object tipo                      | Tipo de parâmetro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | sem suporte  |



 

</dd> <dt>

*DDY* \[ Em\]
</dt> <dd>

Tipo: **float**

A taxa de alteração da geometria da superfície na direção y. O tipo de argumento depende do tipo de objeto de textura.



| Texture-Object tipo                      | Tipo de parâmetro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | sem suporte  |



 

</dd> <dt>

*Deslocamento* \[ Em\]
</dt> <dd>

Tipo: **int**

Um deslocamento de coordenada de textura opcional, que pode ser usado para qualquer tipo de objeto de textura; o deslocamento é aplicado ao local antes da amostragem. Use um deslocamento somente em um miplevel inteiro; caso contrário, você poderá obter resultados que não são bem traduzidos para hardware. O tipo de argumento depende do tipo de objeto de textura. Para obter mais informações, consulte [Aplicando deslocamentos inteiros.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo de parâmetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | sem suporte  |



 

</dd> <dt>

*Fixação* \[ Em\]
</dt> <dd>

Tipo: **float**

Um valor opcional para fixar valores LOD de exemplo. Por exemplo, se você passar 2,0f para o valor de fixação, garantirá que nenhuma amostra individual acesse um nível de mip menor que 2,0f.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; Em vez disso, passe o status para a [**função intrínseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** retornará **TRUE** se todos os valores  da operação de **Exemplo,** **Coletar** ou Carregar correspondente acessarem blocos mapeados em um recurso lado a [lado.](/windows/desktop/direct3d11/direct3d-11-2-features) Se algum valor tiver sido retirado de um tile não mapeado, **CheckAccessFullyMapped** retornará **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

O formato de textura, que é um dos valores digitados listados em [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos SampleGrad](texture2d-samplegrad.md)
</dt> </dl>

 

 
