---
description: Retornará TRUE se o thread atual for o proprietário da seção crítica especificada.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Função CritCheckIn (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752890"
---
# <a name="critcheckin-function"></a>Função CritCheckIn

Retornará **true** se o thread atual for o proprietário da seção crítica especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Ponteiro para uma seção crítica [**CCritSec**](ccritsec.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em builds de depuração, retornará **true** se o thread atual for o proprietário desta seção crítica ou **false** caso contrário. Em compilações de varejo, sempre retorna **true**.

## <a name="remarks"></a>Comentários

Essa função é especialmente útil na macro [**Assert**](assert.md) , para testar se um thread possui um determinado bloqueio.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como usar essa função:


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de depuração de seção crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




