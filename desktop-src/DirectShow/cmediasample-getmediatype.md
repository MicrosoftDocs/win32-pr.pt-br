---
description: 'O método GetMediaType recupera o tipo de mídia, se o tipo de mídia for diferente do exemplo anterior. Esse método implementa o método IMediaSample:: GetMediaType.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Método CMediaSample. GetMediaType (Amfilter. h)
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
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778623"
---
# <a name="cmediasamplegetmediatype-method"></a>Método CMediaSample. GetMediaType

O `GetMediaType` método recuperará o tipo de mídia se o tipo de mídia for diferente do exemplo anterior. Esse método implementa o método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .

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

Endereço de uma variável que recebe um ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Se o tipo de mídia não tiver sido alterado do exemplo anterior, *\* ppMediaType* será definido como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>       | O tipo de mídia não foi alterado do exemplo anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                                     |



 

## <a name="remarks"></a>Comentários

Quando terminar o tipo de mídia, libere o bloco de memória chamando a função do utilitário [**DeleteMediaType**](deletemediatype.md) .

A variável de membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) especifica o tipo de mídia. A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica se o tipo de mídia foi alterado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




