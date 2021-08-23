---
title: Função RWTexture2D::Operator
description: Retorna uma variável de recurso. | Função RWTexture2D::Operator
ms.assetid: 339dba7d-b0c6-4112-ae40-555661577a3e
keywords:
- Função de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da16a89eb704e924931b8d3b4e5144d7154eed50f298aa0606b9b0fb5a45f46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985996"
---
# <a name="rwtexture2doperator--function"></a>Função RWTexture2D::Operator

Retorna uma variável de recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pos* \[ Em\]
</dt> <dd>

Tipo: **uint2**

A posição do índice. Contém as coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **R**

Uma variável de recurso.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWTexture2D](sm5-object-rwtexture2d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




