---
title: 'Buffer:: função GetDimensions'
description: 'Obtém o comprimento do buffer. | Buffer:: função GetDimensions'
ms.assetid: 704890e8-43e4-4e72-b7e2-eeef331bef1c
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
ms.openlocfilehash: d7c56d673e533b4626a57669cf884d80da63d7848cfc7a3e248762f6c4f42088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986096"
---
# <a name="buffergetdimensions-function"></a>Buffer:: função GetDimensions

Obtém o comprimento do buffer.

## <a name="syntax"></a>Sintaxe

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*esmaecer* \[\]
</dt> <dd>

Tipo: **uint**

O comprimento, em bytes, do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




