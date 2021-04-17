---
description: O método getprivadotime recupera o tempo real do relógio.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Método CBaseReferenceClock. getparticulartime (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754556"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>Método CBaseReferenceClock. getparticulartime

O `GetPrivateTime` método recupera o tempo real do relógio.

## <a name="syntax"></a>Sintaxe


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a hora do relógio atual, em unidades de 100 a nanossegundos.

## <a name="remarks"></a>Comentários

Esse método retorna o tempo real relatado pelo relógio. Os chamadores externos usam o método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) , que chama esse método. Ao contrário do método **getTime** , o relógio interno tem permissão para retroceder. Se isso acontecer, o método **getTime** continuará retornando a última vez que ele foi relatado, até que o método se ajuste `GetPrivateTime` .

Esse método retorna a hora do sistema. Substitua esse método se o relógio obtiver o tempo de outra fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




