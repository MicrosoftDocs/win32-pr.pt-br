---
title: Texture2DArray::mips. Função de operador
description: Retorna uma variável de recurso somente leitura. | Texture2DArray::mips. Função de operador
ms.assetid: 66639bf6-74dd-4c69-9cc1-74cc9314de57
keywords:
- Mips. Função de operador HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5dff48f721e45ef7853c125b1d7d0d32d5cb311a3dbc3b31d4100f3038a8fdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724587"
---
# <a name="texture2darraymipsoperator----function"></a>Texture2DArray::mips. Função de operador

Retorna uma variável de recurso somente leitura.

## <a name="syntax"></a>Sintaxe

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mipSlice* \[ Em\]
</dt> <dd>

Tipo: **uint**

O índice de fatia mip.

</dd> <dt>

*pos* \[ Em\]
</dt> <dd>

Tipo: **uint3**

A posição do índice. O primeiro e o segundo componentes contêm as coordenadas (x, y). O terceiro componente indica a fatia de matriz desejada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

### <a name="usage-example"></a>Exemplo de uso


```
Texture2DArray<float4> tex;
uint mip = 2;
uint2 pos_xy_and_array = {123, 456, 3};
float4 f = tex.mips[mip][pos_xy_and_array];
        
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DArray](sm5-object-texture2darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




