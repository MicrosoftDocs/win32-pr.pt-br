---
title: 'Função Texture3D:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função Texture3D:: Operator'
ms.assetid: d7e27778-6a96-47f8-a58a-1966452adf04
keywords:
- Função Operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d701e5f9ba46d17c305fda0a936700e10a1348440e55c913537f2a2d00a5c57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985696"
---
# <a name="texture3doperator--function"></a>Função Texture3D:: Operator

Retorna uma variável de recurso somente leitura.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint3**

A posição do índice. Contém as coordenadas (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

Esse método sempre acessa o primeiro nível de MIP. Para especificar outros níveis de MIP, use o [**MIP \[ \] \[ \] . Operator**](sm5-object-texture3d-mipsoperatorindex.md) .

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




