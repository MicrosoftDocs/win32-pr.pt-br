---
description: Habilita ou desabilita o log de depuração de uma determinada seção crítica.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Função DbgLockTrace (Wxutil. h)
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
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751879"
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

Ponteiro para uma seção crítica [**CCritSec**](ccritsec.md) .

</dd> <dt>

*fTrace* 
</dt> <dd>

Valor que especifica se o log está habilitado. Use **true** para habilitar o registro em log ou **false** para desabilitá-lo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use essa função para rastrear uma seção crítica específica. Por padrão, o log de depuração de seções críticas está desabilitado, devido ao grande número de seções críticas.

Para rastrear uma seção crítica, execute as seguintes etapas:

1.  Defina Depurar ou \_ depurar antes de incluir os cabeçalhos do DirectShow.
2.  Habilite o log de depuração para seções críticas, chamando [**DbgSetModuleLevel**](dbgsetmodulelevel.md) com o sinalizador de bloqueio de log \_ .
3.  Chame **DbgLockTrace** na seção crítica que você deseja rastrear.

Em compilações de varejo, a função **DbgLockTrace** não tem efeito.

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
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de depuração de seção crítica](critical-section-debugging-functions.md)
</dt> </dl>

 

 




