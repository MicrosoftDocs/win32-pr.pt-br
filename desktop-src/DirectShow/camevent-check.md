---
description: O método check verifica se o evento está definido, sem bloqueio.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Método CAMEvent. check (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758887"
---
# <a name="cameventcheck-method"></a>Método CAMEvent. check

O `Check` método verifica se o evento está definido, sem bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
BOOL Check();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

Retornará **true** se o evento for definido ou **false** caso contrário. Esse método chama o método [**CAMEvent:: Wait**](camevent-wait.md) com um tempo limite de zero. Se o objeto for um evento de redefinição automática, esse método redefinirá o evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




