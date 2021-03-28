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
ms.openlocfilehash: c7f1ad1da7600e65d7442c1b2431535e2fdcf38c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968285"
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



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Buffer](sm5-object-buffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




