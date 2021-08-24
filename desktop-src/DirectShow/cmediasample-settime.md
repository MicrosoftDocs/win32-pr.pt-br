---
description: 'O método setTime define os tempos de transmissão quando este exemplo deve começar e terminar. Esse método implementa o método IMediaSample:: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Método CMediaSample. setTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be9028db35cb6d74623bde77fac21e32793de436ea2f80d2f513687c15d1b64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156508"
---
# <a name="cmediasamplesettime-method"></a>Método CMediaSample. setTime

O `SetTime` método define os tempos de transmissão quando este exemplo deve começar e terminar. Esse método implementa o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimeStart* 
</dt> <dd>

Aponta para a hora do fluxo no qual o exemplo começa, em unidades de 100 a nanossegundos ou **NULL**.

</dd> <dt>

*pTimeEnd* 
</dt> <dd>

Aponta para a hora do fluxo em que o exemplo termina, em unidades de 100 nanossegundos ou **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método define as variáveis de membro final [**CMediaSample:: m \_ Start**](cmediasample-m-start.md) e [**CMediaSample:: m \_**](cmediasample-m-end.md) , que especificam os carimbos de data/hora. Ele também atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica se os carimbos de data/hora são válidos.

Para obter informações sobre carimbos de data/hora, consulte [tempo e relógios em DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




