---
title: Função ConsumeStructuredBuffer::Consume
description: Remove um valor do final do buffer.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Consumir função HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a76f8c27ed50c7d7eab1b37cd5c60257691b8db5e5af412f5b3bfe678c283bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486696"
---
# <a name="consume-function"></a>Função Consume

Remove um valor do final do buffer.

## <a name="syntax"></a>Sintaxe

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **T**

O valor removido (pode ser uma estrutura).

## <a name="remarks"></a>Comentários

T pode ser qualquer tipo de dados, incluindo uma estrutura .

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




