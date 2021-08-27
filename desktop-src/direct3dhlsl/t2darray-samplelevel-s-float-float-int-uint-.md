---
title: 'Função SampleLevel:: SampleLevel (S, float, float, int, uint) para Texture2DArray'
description: 'Obtém uma textura no nível de mipmap especificado e retorna o status sobre a operação. Para Texture2DArray. | Função SampleLevel:: SampleLevel (S, float, float, int, uint)'
ms.assetid: 2A561EE4-D7CF-44D4-AC93-F6841770B868
keywords:
- HLSL da função SampleLevel
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b00882702b44b7d4f9ccb101866400cb023cea00be637e898d9ecd71ed2e262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118046"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2darray"></a>Função SampleLevel:: SampleLevel (S, float, float, int, uint) para Texture2DArray

Obtém uma textura no nível de mipmap especificado e retorna o status sobre a operação.

## <a name="syntax"></a>Sintaxe


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
  out uint         Status
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

*LOD* \[ no\]
</dt> <dd>

Tipo: **float**

\[em \] um número que especifica o nível de mipmap. Se o valor for ≤ 0, o nível de mipmap 0 (maior mapa) será usado. O valor fracionário (se fornecido) é usado para interpolar entre dois níveis de mipmap.

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

*Status* \[ do fora\]
</dt> <dd>

Tipo: **uint**

O status da operação. Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features). Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

O formato de textura, que é um dos valores tipados listados [**no \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos SampleLevel](texture2darray-samplelevel.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
