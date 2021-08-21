---
description: O método OnThreadDestroy é chamado quando o thread de streaming está prestes a sair.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Método CSourceStream.OnThreadDestroy (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71bd7ff9da79ed42ad7d36ff176a60687ca5fd0edcd6003d77c20084adc1b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953695"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Método CSourceStream.OnThreadDestroy

O `OnThreadDestroy` método é chamado quando o thread de streaming está prestes a sair.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O procedimento de thread, [**CSourceStream::ThreadProc,**](csourcestream-threadproc.md)chama esse método antes de sair. O método não faz nada na classe base; ele está disponível para a classe derivada substituir. Se a classe derivada retornar um código de erro, o thread será final com um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




