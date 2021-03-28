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
ms.openlocfilehash: 1a73577fa67992b212b4769059f1523e584acbaf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172869"
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

## <a name="return-value"></a>Retornar valor

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



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




