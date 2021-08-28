---
title: 'Função Texture1DArray:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função Texture1DArray:: Operator'
ms.assetid: 05ec9652-b5dd-41cf-8bef-730c507c5ba4
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
ms.openlocfilehash: ed214b4c4ccc55dfe6500f70659f4f81b2188de68b8cea7b5ba69c495108d730
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788346"
---
# <a name="texture1darrayoperator--function"></a>Função Texture1DArray:: Operator

Retorna uma variável de recurso somente leitura.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint2**

A posição do índice. O primeiro componente contém a coordenada x. O segundo componente indica a fatia de matriz desejada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

Esse método sempre acessa o primeiro nível de MIP. Para especificar outros níveis de MIP, use o método [**MIP \[ \] \[ \] . Operator**](sm5-object-texture1darray-mipsoperatorindex.md) em vez disso.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture1DArray](sm5-object-texture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




