---
title: 'Função RWBuffer:: Load (int)'
description: 'Lê dados de buffer. | Função RWBuffer:: Load (int)'
ms.assetid: 3066E244-DE56-4F0D-8443-018B9EFEC1FF
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
ms.openlocfilehash: 561f055990bbca683bf9c55b5805b8d3c55b3272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663886"
---
# <a name="rwbufferloadint-function"></a>Função RWBuffer:: Load (int)

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

O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWBuffer**](sm5-object-rwbuffer.md) .

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwbuffer-load.md)
</dt> </dl>

 

 




