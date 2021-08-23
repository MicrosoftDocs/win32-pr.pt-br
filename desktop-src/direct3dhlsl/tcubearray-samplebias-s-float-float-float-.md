---
title: Função SampleBias::SampleBias(S,float,float,float) para TextureCubeArray
description: A função SampleBias::SampleBias(S,float,float,float) para TextureCubeArray amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap.
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
keywords:
- Função SampleBias HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea7c030ca1a99e9d9169ac4e20c26fbb352d199f471be2f926f758c87374b092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043130"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a>Função SampleBias::SampleBias(S,float,float,float) para TextureCubeArray

Amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap, com um valor opcional para fixar valores lod (nível de detalhes) de exemplo.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
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

*Desvio* \[ Em\]
</dt> <dd>

Tipo: **float**

O valor de desvio, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de mip antes da amostragem.

</dd> <dt>

*Fixação* \[ Em\]
</dt> <dd>

Tipo: **float**

Um valor opcional para fixar valores LOD de exemplo. Por exemplo, se você passar 2,0f para o valor de fixação, garantirá que nenhuma amostra individual acesse um nível de mip menor que 2,0f.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

O formato de textura, que é um dos valores digitados listados em [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos SampleBias](texturecubearray-samplebias.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
