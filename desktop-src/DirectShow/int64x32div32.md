---
description: A função Int64x32Div32 implementa a fórmula ((a \* b) + Rnd)/c, em que um é um valor de 64 bits e b, c e Rnd são valores de 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Função Int64x32Div32 (Wxutil. h)
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
ms.openlocfilehash: a56425d1f07346f8e546940ff5880416e4e63efc692974c78f0e344b9ec01c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051586"
---
# <a name="int64x32div32-function"></a>Função Int64x32Div32

A `Int64x32Div32` função implementa a fórmula `((a*b)+rnd)/c` em que *um* é um valor de 64 bits e *b*, *c* e *Rnd* são valores de 32 bits.

## <a name="syntax"></a>Sintaxe


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
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

## <a name="return-value"></a>Valor retornado

Retorna o `(a * b + rnd)/c` cálculo ou um dos valores a seguir.



| Código de retorno                                                                                       | Descrição                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Ocorreu um estouro porque o resultado é muito grande (positivo).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Ocorreu um estouro porque o resultado é muito grande (negativo).<br/> |



 

## <a name="remarks"></a>Comentários

O arredondamento na divisão é diferente de zero. A divisão por zero é contada como uma condição de estouro.

Carimbos de data/hora e tempos de busca são valores de 64 bits, portanto, essa função é útil para executar conversões em sistemas de 32 bits. Por exemplo, em MPEG-1, a referência do relógio do sistema é 90-kHz ou 90.000 tiques por segundo. A fórmula para converter isso em tempo de referência (unidades de 100 a nanossegundos) é


```C++
(timestamp * 1000) / 9
```



que pode ser calculado como `Int64x32Div32(timestamp, 1000, 9, 0)` . Use o parâmetro *Rnd* como um fator de arredondamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




