---
title: 'Função RWTexture2DArray:: Operator'
description: 'Retorna uma variável de recurso. | Função RWTexture2DArray:: Operator'
ms.assetid: ae3d0697-ea0a-450d-bdfe-7bc5d8faf11a
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
ms.openlocfilehash: faf49c48fbf5042ce2765005cd8daea4d1227255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104011989"
---
# <a name="rwtexture2darrayoperator--function"></a>Função RWTexture2DArray:: Operator

Retorna uma variável de recurso.

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

A posição do índice. O primeiro e o segundo componentes contêm as coordenadas (x, y). O terceiro componente indica a fatia de matriz desejada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWTexture2DArray](sm5-object-rwtexture2darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




