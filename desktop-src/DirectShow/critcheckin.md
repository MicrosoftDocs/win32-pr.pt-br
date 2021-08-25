---
description: Retornará TRUE se o thread atual for o proprietário da seção crítica especificada.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Função CritCheckIn (Wxutil.h)
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
ms.openlocfilehash: 4f4e9ff0078f6efe8dee9b060e61858c24aea0a64e7e35b9fb867125b8612ed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908076"
---
# <a name="critcheckin-function"></a>Função CritCheckIn

Retornará **TRUE** se o thread atual for o proprietário da seção crítica especificada.

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

Ponteiro para uma [**seção crítica CCritSec.**](ccritsec.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em builds de depuração, **retornará TRUE** se o thread atual for o proprietário desta seção crítica ou **FALSE** caso contrário. Em builds de varejo, sempre retorna **TRUE.**

## <a name="remarks"></a>Comentários

Essa função é especialmente útil dentro da macro [**ASSERT,**](assert.md) para testar se um thread possui um determinado bloqueio.

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
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções críticas de depuração de seção](critical-section-debugging-functions.md)
</dt> </dl>

 

 




