---
title: Função RWBuffer::GetDimensions
description: Obtém o comprimento do buffer. | Função RWBuffer::GetDimensions
ms.assetid: 600147cb-9513-4b74-a873-1ed22b31cdf7
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 586f266fea0dbc035e8ff3a61e39cb18a7102d792ee05c44345a1b702cc1b574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118236"
---
# <a name="rwbuffergetdimensions-function"></a>Função RWBuffer::GetDimensions

Obtém o comprimento do buffer.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*esmaecimento* \[\]
</dt> <dd>

Tipo: **uint**

O comprimento, em bytes, do buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Nada

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWBuffer](sm5-object-rwbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




