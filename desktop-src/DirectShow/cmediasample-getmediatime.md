---
description: 'O método GetMediaTime recupera os horários de mídia para este exemplo. Esse método implementa o método IMediaSample:: GetMediaTime.'
ms.assetid: f58a2162-5764-48f2-8984-ee4bba1229ab
title: Método CMediaSample. GetMediaTime (Amfilter. h)
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
ms.openlocfilehash: f9a41d29e46d29cff9023421a661cc90731d4c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757704"
---
# <a name="cmediasamplegetmediatime-method"></a>Método CMediaSample. GetMediaTime

O `GetMediaTime` método recupera os horários de mídia para este exemplo. Esse método implementa o método [**IMediaSample:: GetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaTime(
   LONGLONG *pStart,
   LONGLONG *pEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início da mídia.

</dd> <dt>

*Pendente* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de parada da mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                         |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ hora de mídia \_ \_ não \_ definida**</dt> </dl> | Nenhum horário de mídia foi definido para este exemplo.<br/> |



 

## <a name="remarks"></a>Comentários

A variável de membro [**CMediaSample:: m \_ MediaEnd**](cmediasample-m-mediaend.md) especifica um deslocamento [**de CMediaSample:: m \_ MediaStart**](cmediasample-m-mediastart.md), mas o valor recebido pelo parâmetro *pendente* é um tempo de mídia absoluto, calculado como **m \_ MediaStart**  +  **m \_ MediaEnd**.

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

 

 




