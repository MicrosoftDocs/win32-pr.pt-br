---
title: 'Função Texture1D:: Operator'
description: Retorna uma variável de recurso somente leitura para um Texture1D.
ms.assetid: df54097d-4d1b-496a-a17d-6e9a10cfb996
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
ms.openlocfilehash: d2c11ef313531adb9b129ffb99103ea6c7778462eddf8c1c76f4b235c92951c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985906"
---
# <a name="texture1doperator--function"></a>Função Texture1D:: Operator

Retorna uma variável de recurso somente leitura para um [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ no\]
</dt> <dd>

Tipo: **uint**

A posição do índice. Contém a coordenada x.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso somente leitura.

## <a name="remarks"></a>Comentários

Esse método sempre acessa o primeiro nível de MIP. Para especificar outros níveis de MIP, use o [**MIP. \[ \] \[ \] Operator**](sm5-object-texture1d-mipsoperatorindex.md) em vez disso.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




