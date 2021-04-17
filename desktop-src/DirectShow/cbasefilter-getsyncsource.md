---
description: 'O método getsyncprovider recupera o relógio de referência que o filtro está usando. Esse método implementa o método IMediaFilter:: getsync.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Método CBaseFilter. getsyncize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749639"
---
# <a name="cbasefiltergetsyncsource-method"></a>Método CBaseFilter. getsyncize

O `GetSyncSource` método recupera o relógio de referência que o filtro está usando. Esse método implementa o método [**IMediaFilter:: getsync**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

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

Se o filtro não estiver usando um relógio de referência, *\* pClock* será definido como **NULL**. Quando o método retornar, se *\* pClock* for não **nulo**, a interface **IReferenceClock** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




