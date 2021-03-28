---
title: 'Texture3D:: MIPS. Função Operator'
description: 'Retorna uma variável de recurso somente leitura. | Texture3D:: MIPS. Função Operator'
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
keywords:
- seqüencia. Função Operator HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8f7064459354ec4827ba6d96795e82ccab3800c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172677"
---
# <a name="texture3dmipsoperator----function"></a>Texture3D:: MIPS. Função Operator

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

*mipSlice* \[ no\]
</dt> <dd>

Tipo: **uint**

O índice de fatia MIP.

</dd> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint3**

A posição do índice. Contém as coordenadas (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

### <a name="usage-example"></a>Exemplo de uso


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




