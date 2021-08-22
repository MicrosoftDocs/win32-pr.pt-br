---
title: 'Texture2DMS:: sample. Função Operator'
description: 'Recupera um valor do recurso no local e no índice de exemplo fornecidos. | Texture2DMS:: sample. Função Operator'
ms.assetid: 5bc24129-b690-44dd-ae85-8533b10befaa
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
ms.openlocfilehash: 8f5d7082ee72c49d3aa4be131491151b1bab65502e6fe85884b2a03573c497b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508468"
---
# <a name="texture2dmssampleoperator----function"></a>Texture2DMS:: sample. Função Operator

Recupera um valor do recurso no local e no índice de exemplo fornecidos.

## <a name="syntax"></a>Sintaxe

``` syntax
R sample.Operator[][](
  in uint sampleSlice,
  in uint2 pos
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

Tipo: **uint2**

A posição do índice. Os componentes contêm as coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

### <a name="usage-example"></a>Exemplo de uso


```
Texture2DMS<float4, 8> tex;

float4 main( float3 tcoord : texturecoord0 ) : SV_Target
{
     return s_msTexture.sample[2][tcoord];
}
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




