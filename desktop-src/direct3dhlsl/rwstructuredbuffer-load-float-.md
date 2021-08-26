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
ms.openlocfilehash: e3cc8fbd0cfa18f2ac6c5d7109e8690d829bbde2175e8808865e68e29e63c955
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067747"
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

## <a name="return-value"></a>Valor retornado

Tipo:

O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md) .

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](rwstructuredbuffer-load.md)
</dt> </dl>

 

 




