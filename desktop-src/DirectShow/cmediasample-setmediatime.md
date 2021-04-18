---
description: 'O método SetMediaTime define as horas de mídia para este exemplo. Esse método implementa o método IMediaSample:: SetMediaTime.'
ms.assetid: 768812f8-c044-4499-9149-7c334c51e539
title: Método CMediaSample. SetMediaTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0240ef40f4c37f6c5528c979b2e89b43b03b3451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756198"
---
# <a name="cmediasamplesetmediatime-method"></a>Método CMediaSample. SetMediaTime

O `SetMediaTime` método define os horários de mídia para este exemplo. Esse método implementa o método [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Ponteiro para a hora de início da mídia ou **nulo**.

</dd> <dt>

*Pendente* 
</dt> <dd>

Ponteiro para a hora de parada da mídia ou **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

A hora de parada da mídia deve ser maior que a hora de início da mídia. Use **NULL** para invalidar os horários de mídia.

O parâmetro *pendente* especifica um tempo de mídia absoluto, mas a variável de membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) é calculada como um deslocamento de *PStart*. Em outras palavras, **m \_ MediaEnd**  =  \* *pTimeEnd* \* *pTimeStart*.  

Para obter informações sobre os tempos de mídia, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




