---
description: 'O método getsyncprovider recupera o relógio de referência que o objeto está usando. Esse método implementa o método IMediaFilter:: getsync.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Método CBaseMediaFilter. getsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748227"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Método CBaseMediaFilter. getsyncize

O `GetSyncSource` método recupera o relógio de referência que o objeto está usando. Esse método implementa o método [**IMediaFilter:: getsync**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClock* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="remarks"></a>Comentários

Se o objeto não estiver usando um relógio de referência, *\* pClock* será definido como **NULL**. Quando o método retornar, se *\* pClock* for não **nulo**, a interface **IReferenceClock** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




