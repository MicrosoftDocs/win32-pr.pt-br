---
description: O método SetSyncSource define um relógio de referência para o filtro. Esse método implementa o método IMediaFilter::SetSyncSource.
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Método CBaseFilter.SetSyncSource (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95e1f1b3578fa88d4616fc9e0b7d0af9fe89ab80c2e93ee32eef305b93d45478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659582"
---
# <a name="cbasefiltersetsyncsource-method"></a>Método CBaseFilter.SetSyncSource

O **método SetSyncSource** define um relógio de referência para o filtro. Esse método implementa o [**método IMediaFilter::SetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource)

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

Ponteiro para a interface [**IReferenceClock do**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) relógio ou **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




