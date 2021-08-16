---
description: O método getschedule recupera um ponteiro para o objeto de agendamento do relógio.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: Método CBaseReferenceClock. getschedule (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6be5c4ed76573428967138682b478a54859e4ca97213f132ff805a0e83be0b50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822832"
---
# <a name="cbasereferenceclockgetschedule-method"></a>Método CBaseReferenceClock. getschedule

O `GetSchedule` método recupera um ponteiro para o objeto de agendamento do relógio.

## <a name="syntax"></a>Sintaxe


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a variável de membro [**CBaseReferenceClock:: m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




