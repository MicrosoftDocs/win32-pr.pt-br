---
title: 'Texture2DMSArray:: sample. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture2DMSArray:: sample. Função Operator'
ms.assetid: 5334c1d5-dfbd-4987-875c-0b92967b0f13
keywords:
- Nova. Função Operator HLSL
topic_type:
- apiref
api_name:
- sample.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e78746e0afe03e65a313982ca35c27a75ea14f1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968516"
---
# <a name="texture2dmsarraysampleoperator----function"></a>Texture2DMSArray:: sample. Função Operator

Retorna uma variável de recurso somente leitura.

## <a name="syntax"></a>Sintaxe

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sampleSlice* \[ no\]
</dt> <dd>

Tipo: **uint**

O índice de fatia de exemplo.

</dd> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint3**

A posição do índice. O primeiro e o segundo componentes contêm as coordenadas (x, y). O terceiro componente indica a fatia de matriz desejada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

### <a name="usage-example"></a>Exemplo de uso


```
Texture2DMSArray<float4, 4> alpha;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




