---
title: 'Função RWStructuredBuffer:: Load (int)'
description: 'Lê dados de buffer. | Função RWStructuredBuffer:: Load (int)'
ms.assetid: 9CB40579-6BF8-468C-81B8-936D9940458E
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c20998faef8f5a018aaf95571be3c9d64730c436
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989154"
---
# <a name="rwstructuredbufferloadint-function"></a>Função RWStructuredBuffer:: Load (int)

Lê dados de buffer.

## <a name="syntax"></a>Sintaxe


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Local* \[ do no\]
</dt> <dd>

Tipo: **int**

O local do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




