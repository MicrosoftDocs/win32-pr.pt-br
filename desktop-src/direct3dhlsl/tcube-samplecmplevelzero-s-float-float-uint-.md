---
title: Função SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) para TextureCube
description: Amostra apenas uma textura no nível 0 do mipmap e compara o resultado com um valor de comparação. Retorna o status sobre a operação. Para TextureCube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
keywords:
- Função SampleCmpLevelZero HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5970b2a03a3004269b8ef758569aa6ac222bb60032dcb91e121a342e58cef886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117986"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a>Função SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) para TextureCube

Amostra apenas uma textura no nível 0 do mipmap e compara o resultado com um valor de comparação. Retorna o status sobre a operação.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

*CompareValue* \[ Em\]
</dt> <dd>

Tipo: **float**

Um valor de ponto flutuante a ser usado como um valor de comparação.

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

[Métodos SampleCmpLevelZero](texturecube-samplecmplevelzero.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
