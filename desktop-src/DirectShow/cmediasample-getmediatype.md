---
description: O método GetMediaType recuperará o tipo de mídia, se o tipo de mídia for diferente do exemplo anterior. Esse método implementa o método IMediaSample::GetMediaType.
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Método CMediaSample.GetMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee7b5464ff2620dbc0247b006dc323232131de3936d2c5e56f2232b67c00ba5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832296"
---
# <a name="cmediasamplegetmediatype-method"></a>Método CMediaSample.GetMediaType

O `GetMediaType` método recupera o tipo de mídia, se o tipo de mídia for diferente do exemplo anterior. Esse método implementa o [**método IMediaSample::GetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMediaType* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para uma estrutura [**AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Se o tipo de mídia não tiver sido alterado do exemplo anterior, *\* ppMediaType* será definido como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | O tipo de mídia não foi alterado do exemplo anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                                     |



 

## <a name="remarks"></a>Comentários

Quando você terminar o tipo de mídia, livre o bloco de memória chamando a função de utilitário [**DeleteMediaType.**](deletemediatype.md)

A variável de membro [**CMediaSample::m \_ pMediaType**](cmediasample-m-pmediatype.md) especifica o tipo de mídia. A [**variável de membro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica se o tipo de mídia foi alterado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




