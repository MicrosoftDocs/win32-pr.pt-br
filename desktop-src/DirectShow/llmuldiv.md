---
description: A função llMulDiv implementa a fórmula ((a \* b) + Rnd)/c, em que cada termo é um valor de 64 bits.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: função llMulDiv (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780859"
---
# <a name="llmuldiv-function"></a>função llMulDiv

A `llMulDiv` função implementa a fórmula `((a*b)+rnd)/c` em que cada termo é um valor de 64 bits.

Carimbos de data/hora e tempos de busca são valores de 64 bits, portanto, essa função é útil para executar conversões em sistemas de 32 bits. Por exemplo, a fórmula para bytes por segundo é


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



que pode ser calculado como `llMulDiv(nBytes, rtTime, 10000000, 0)` . Use o parâmetro *Rnd* como um fator de arredondamento.

## <a name="syntax"></a>Sintaxe


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*um* 
</dt> <dd>

Multiplicando.

</dd> <dt>

*b* 
</dt> <dd>

Multiplicador.

</dd> <dt>

*c* 
</dt> <dd>

Divisor.

</dd> <dt>

*Rnd* 
</dt> <dd>

Fator de arredondamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o `(a * b + rnd)/c` cálculo ou um dos valores a seguir.



| Código de retorno                                                                                       | Descrição                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Ocorreu um estouro porque o resultado é muito grande (positivo).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Ocorreu um estouro porque o resultado é muito grande (negativo).<br/> |



 

## <a name="remarks"></a>Comentários

O arredondamento na divisão é diferente de zero. A divisão por zero é contada como uma condição de estouro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




