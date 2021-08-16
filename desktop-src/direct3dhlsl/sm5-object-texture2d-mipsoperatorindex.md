---
title: Texture2D::mips. Função de operador
description: Retorna uma variável de recurso somente leitura. | Texture2D::mips. Função de operador
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 0d8c915c340e69eedc8b66a1665b6e600c0134b66cb6cd81fe6b803681e5fdeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789492"
---
# <a name="texture2dmipsoperator----function"></a>Texture2D::mips. Função de operador

Retorna uma variável de recurso somente leitura.

## <a name="syntax"></a>Sintaxe

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
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

Tipo: **uint2**

A posição do índice. Contém as coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

### <a name="usage-example"></a>Exemplo de uso


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




