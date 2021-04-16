---
description: O método OnThreadDestroy é chamado quando o thread de streaming está prestes a sair.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Método CSourceStream. OnThreadDestroy (Source. h)
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
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750280"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Método CSourceStream. OnThreadDestroy

O `OnThreadDestroy` método é chamado quando o thread de streaming está prestes a sair.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O procedimento de thread, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), chama esse método antes de sair. O método não faz nada na classe base; Ele está disponível para a classe derivada substituir. Se a classe derivada retornar um código de erro, o thread será encerrado com um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




