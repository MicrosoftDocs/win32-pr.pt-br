---
title: Função SampleCmp::SampleCmp(S,float,float,float) para TextureCube
description: Amostra uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixar valores de LOD (nível de detalhes) de exemplo. | Função SampleCmp::SampleCmp(S,float,float,float) para TextureCube
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
keywords:
- Função SampleCmp HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d46ab1adc7e5ce84d1cc8e8673babd5f24fb2afe33a620162fa757d5650053e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506551"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a>Função SampleCmp::SampleCmp(S,float,float,float) para TextureCube

Amostra uma textura, usando um valor de comparação para rejeitar amostras, com um valor opcional para fixar valores de LOD (nível de detalhes) de exemplo.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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

*CompareValue* \[ Em\]
</dt> <dd>

Tipo: **float**

Um valor de ponto flutuante a ser usado como um valor de comparação.

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

[Métodos SampleCmp](texturecube-samplecmp.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
