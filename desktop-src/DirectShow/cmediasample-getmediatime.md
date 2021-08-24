---
description: O método GetMediaTime recupera os tempos de mídia para este exemplo. Esse método implementa o método IMediaSample::GetMediaTime.
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Método CMediaSample.GetMediaTime (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901531b3aaff882700a6a6196330cc7b0823b8b0069024101953f5f79a54e17d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634676"
---
# <a name="cmediasamplegetmediatime-method"></a>Método CMediaSample.GetMediaTime

O `GetMediaTime` método recupera os tempos de mídia para este exemplo. Esse método implementa o [**método IMediaSample::GetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início da mídia.

</dd> <dt>

*Pend* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de parada da mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                 |
| <dl> <dt>**TEMPO DE MÍDIA DO VFW \_ E \_ NÃO \_ \_ \_ DEFINIDO**</dt> </dl> | Nenhum horário de mídia foi definido para este exemplo.<br/> |



 

## <a name="remarks"></a>Comentários

A variável membro [**CMediaSample::m \_ MediaEnd**](cmediasample-m-mediaend.md) especifica um deslocamento de [**CMediaSample::m \_ MediaStart**](cmediasample-m-mediastart.md), mas o valor recebido pelo parâmetro *pEnd* é um tempo de mídia absoluto, calculado como **m \_ MediaStart**  +  **m \_ MediaEnd**.

Para obter informações sobre os tempos de mídia, consulte [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




