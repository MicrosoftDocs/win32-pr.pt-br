---
description: O método Lock bloqueia o objeto da seção crítica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Método CCritSec. Lock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778506"
---
# <a name="ccritseclock-method"></a>Método CCritSec. Lock

O método **Lock** bloqueia o objeto da seção crítica.

## <a name="syntax"></a>Sintaxe


```C++
void Lock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método chama a função [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .

Chame a função de membro [**CCritSec:: Unlock**](ccritsec-unlock.md) para desbloquear a seção crítica. Você pode fazer várias chamadas para o método **Lock** no mesmo thread; Não se esqueça de chamar **desbloquear** um número de vezes correspondente.

Se o objeto já estiver bloqueado por outro thread, o método **CCritSec:: Lock** bloqueará até que o objeto seja liberado ou até que ocorra uma exceção de deadlock possível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

