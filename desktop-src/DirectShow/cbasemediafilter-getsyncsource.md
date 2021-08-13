---
description: O método GetSyncSource recupera o relógio de referência que o objeto está usando. Esse método implementa o método IMediaFilter::GetSyncSource.
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Método CBaseMediaFilter.GetSyncSource (Amfilter.h)
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
ms.openlocfilehash: 03bceee63109dedbf3b2fa9a855ddbfb410014d48de613f95c7bbfb98d6b0894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658869"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Método CBaseMediaFilter.GetSyncSource

O `GetSyncSource` método recupera o relógio de referência que o objeto está usando. Esse método implementa o [**método IMediaFilter::GetSyncSource.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)

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

Endereço de uma variável que recebe um ponteiro para a interface [**IReferenceClock do**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) relógio.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="remarks"></a>Comentários

Se o objeto não estiver usando um relógio de referência, *\* pClock* será definido como **NULL.** Quando o método retorna, se *\* pClock* for não **NULL,** a interface **IReferenceClock** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




