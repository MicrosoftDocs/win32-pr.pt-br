---
title: Função SampleBias::SampleBias(S,float,float,int,float) para Texture3D
description: A função SampleBias::SampleBias(S, float,float,int,float) para Texture3D amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap.
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
ms.openlocfilehash: 023c50c2f7233acddf6a289f1a62df466d85e30c1402e9769d36b26746a8542e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723534"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture3d"></a>Função SampleBias::SampleBias(S,float,float,int,float) para Texture3D

Amostra uma textura, depois de aplicar o valor de desvio ao nível de mipmap, com um valor opcional para fixar valores lod (nível de detalhes) de exemplo.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
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

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

O formato de textura, que é um dos valores digitados listados em [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos SampleBias](texture3d-samplebias.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
