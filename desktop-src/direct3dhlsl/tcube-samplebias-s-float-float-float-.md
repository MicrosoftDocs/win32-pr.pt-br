---
title: 'Função SampleBias:: SampleBias (S, float, float, float)'
description: 'Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para. | Função SampleBias:: SampleBias (S, float, float, float)'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
keywords:
- HLSL da função SampleBias
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ae1c14903748f53d9890ff1a4dd9bd806caececf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012039"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a>Função SampleBias:: SampleBias (S, float, float, float)

Amostra uma textura, depois de aplicar o valor de tendência ao nível de mipmap, com um valor opcional para fixe de exemplo de valores de LOD (nível de detalhe) para.

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

*Tendência* \[ no\]
</dt> <dd>

Tipo: **float**

O valor de tendência, que é um número de ponto flutuante entre 0,0 e 1,0, inclusive, é aplicado a um nível de MIP antes da amostragem.

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

[Métodos SampleBias](texturecube-samplebias.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
