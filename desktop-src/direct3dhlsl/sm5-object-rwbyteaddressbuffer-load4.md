---
title: 'Função RWByteAddressBuffer:: Load4 (UINT)'
description: 'Obtém quatro valores. | Função RWByteAddressBuffer:: Load4 (UINT)'
ms.assetid: b46cd119-75be-4c2d-82f9-5dcabd7e4400
keywords:
- HLSL da função Load4
topic_type:
- apiref
api_name:
- Load4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7545c27ccd5f82b3fed1f36a1cc2b0f9d92a9d901f5614ba3b6bec4068cb8abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724966"
---
# <a name="rwbyteaddressbufferload4uint-function"></a>Função RWByteAddressBuffer:: Load4 (UINT)

Obtém quatro valores.

## <a name="syntax"></a>Sintaxe

``` syntax
uint4 Load4(
  in uint address
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*endereço* \[ no\]
</dt> <dd>

Tipo: **uint**

O endereço de entrada em bytes, que deve ser um múltiplo de 4.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint4**

Quatro valores.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos Load4](rwbyteaddressbuffer-load4.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




