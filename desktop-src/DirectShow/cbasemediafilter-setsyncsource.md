---
description: 'O método setsyncprovider define um relógio de referência para o objeto. Esse método implementa o método IMediaFilter:: setsincronizate.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Método CBaseMediaFilter. setsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748644"
---
# <a name="cbasemediafiltersetsyncsource-method"></a>Método CBaseMediaFilter. setsyncize

O `SetSyncSource` método define um relógio de referência para o objeto. Esse método implementa o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClock* 
</dt> <dd>

Ponteiro para a interface [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) do relógio ou **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




