---
description: O método GetRequestParam recupera a solicitação mais recente.
ms.assetid: f5bf4935-29ea-45b9-a57e-9fdcd9cde20a
title: Método CAMThread.GetRequestParam (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestParam
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c511fdb68bb6ee9372530d9e19290342a57fbcc5817148613d20fd8afe029b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384916"
---
# <a name="camthreadgetrequestparam-method"></a>Método CAMThread.GetRequestParam

O `GetRequestParam` método recupera a solicitação mais recente.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetRequestParam() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor do parâmetro que foi passado mais recentemente para o [**método CAMThread::CallWorker.**](camthread-callworker.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMThread**](camthread.md)
</dt> </dl>

 

 




