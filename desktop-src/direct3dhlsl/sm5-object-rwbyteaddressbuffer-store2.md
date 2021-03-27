---
title: 'Função RWByteAddressBuffer:: Store2'
description: Define dois valores.
ms.assetid: 7b32c84c-9ea2-47ae-a0f3-df6d95249163
keywords:
- HLSL da função Store2
topic_type:
- apiref
api_name:
- Store2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 574ad7fd59921767308e980e645bac966be87709
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104006788"
---
# <a name="store2-function"></a>Função Store2

Define dois valores.

## <a name="syntax"></a>Sintaxe

``` syntax
void Store2(
  in uint address,
  in uint2 values
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*endereço* \[ no\]
</dt> <dd>

Tipo: **uint**

O endereço de entrada em bytes, que deve ser um múltiplo de 4.

</dd> <dt>

*valores* \[ de no\]
</dt> <dd>

Tipo: **uint2**

Dois valores de entrada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[RWByteAddressBuffer](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




