---
description: O método AlignDown Trunca um valor para um limite de alinhamento especificado.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Método CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789700"
---
# <a name="cpullpinaligndown-method"></a>Método CPullPin. AlignDown

O `AlignDown` método Trunca um valor para um limite de alinhamento especificado.

## <a name="syntax"></a>Sintaxe


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*precisa* 
</dt> <dd>

Especifica o número a ser alinhado.

</dd> <dt>

*lAlign* 
</dt> <dd>

Especifica o limite de alinhamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o resultado alinhado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




