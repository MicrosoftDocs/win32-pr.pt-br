---
title: 'Função Texture2DArray:: Sample (S, float, int, float)'
description: 'Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para. | Função Texture2DArray:: Sample (S, float, int, float)'
ms.assetid: F6638224-0993-4F55-A8C0-7EC4140204D5
keywords:
- Exemplo de função HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d7405bf1da94d56a8ca8097f912bd1ee9972c8c2d84da379e934942586544005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023326"
---
# <a name="texture2darraysamplesfloatintfloat-function"></a>Função Texture2DArray:: Sample (S, float, int, float)

Amostras de uma textura com um valor opcional para fixe os valores de nível de detalhe (LOD) de exemplo para.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*S* \[ em\]
</dt> <dd>

Um [estado de amostra](dx-graphics-hlsl-sampler.md). Este é um objeto declarado em um arquivo de efeito que contém atribuições de estado.

</dd> <dt>

*Local* \[ do no\]
</dt> <dd>

As coordenadas de textura. O tipo de argumento é dependente do tipo de objeto Texture.



| Tipo de Texture-Object                    | Tipo de parâmetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Deslocamento* \[ no\]
</dt> <dd>

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

Um valor opcional para fixe os valores de LOD de exemplo para. Por exemplo, se você passar 2.0 f para o valor fixe, certifique-se de que nenhum exemplo individual acessa um nível de MIP menor que 2,0 f.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de exemplo](texture2darray-sample.md)
</dt> </dl>

 

 
