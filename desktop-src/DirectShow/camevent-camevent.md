---
description: Método de construtor.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Construtor CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756212"
---
# <a name="cameventcamevent-constructor"></a>Construtor CAMEvent. CAMEvent

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fManualReset* 
</dt> <dd>

Valor booliano que especifica se o objeto é um evento de redefinição manual ou um evento de redefinição automática. Se for **true**, o objeto será um evento de redefinição manual. Caso contrário, é um evento de redefinição automática.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Se o Construtor falhar, esse parâmetro receberá um código de erro. Se isso ocorrer, o objeto não está em um estado válido.

Para compatibilidade com versões anteriores do Strmbase. lib, esse parâmetro assume **nulo** como padrão. No entanto, a passagem de um valor não **nulo** é preferida, para que o chamador possa verificar o status do objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

O evento começa em um estado não sinalizado.

Com um evento de redefinição automática, o método [**CAMEvent:: Wait**](camevent-wait.md) redefine o evento para não sinalizado quando o método retorna. Com um evento de redefinição manual, o evento permanece sinalizado até que você chame o método [**CAMEvent:: Reset**](camevent-reset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




