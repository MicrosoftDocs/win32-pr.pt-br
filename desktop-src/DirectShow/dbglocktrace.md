---
description: Habilita ou desabilita o log de depuração de uma determinada seção crítica.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Função DbgLockTrace (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b55736b2efb8fd4cfbca40710caa930c200c84e1ceec9c8c4f7439468c1add1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654066"
---
# <a name="dbglocktrace-function"></a>Função DbgLockTrace

Habilita ou desabilita o log de depuração de uma determinada seção crítica.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcCrit* 
</dt> <dd>

Ponteiro para uma [**seção crítica CCritSec.**](ccritsec.md)

</dd> <dt>

*fTrace* 
</dt> <dd>

Valor que especifica se o registro em log está habilitado. Use **TRUE para** habilitar o registro em log ou **FALSE** para desabilitá-lo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use essa função para rastrear uma seção crítica específica. Por padrão, o log de depuração de seções críticas está desabilitado, devido ao grande número de seções críticas.

Para rastrear uma seção crítica, execute as seguintes etapas:

1.  Defina DEBUG ou \_ DEBUG antes de incluir os DirectShow de dados.
2.  Habilita o log de depuração para seções críticas chamando [**DbgSetModuleLevel**](dbgsetmodulelevel.md) com o sinalizador LOG \_ LOCKING.
3.  Chame **DbgLockTrace** na seção crítica que você deseja rastrear.

Em builds de varejo, a **função DbgLockTrace** não tem nenhum efeito.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como rastrear uma seção crítica.


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
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

 

 




