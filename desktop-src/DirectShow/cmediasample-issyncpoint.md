---
description: 'O método IsSyncPoint determina se o início do exemplo é um ponto de sincronização. Esse método implementa o método IMediaSample:: IsSyncPoint.'
ms.assetid: e57f78f4-7bb9-4e23-bcb4-55ad7ab5482c
title: Método CMediaSample. IsSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 00d238bb9289ba71237bfdf8e72acde384430f72470f16211093cb2ece8d68f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074000"
---
# <a name="cmediasampleissyncpoint-method"></a>Método CMediaSample. IsSyncPoint

O `IsSyncPoint` método determina se o início do exemplo é um ponto de sincronização. Esse método implementa o método [**IMediaSample:: IsSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-issyncpoint) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsSyncPoint();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se o exemplo for um ponto de sincronização, \_ caso contrário, s false.

## <a name="remarks"></a>Comentários

A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




