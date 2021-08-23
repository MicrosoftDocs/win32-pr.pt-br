---
description: 'O método SetMediaType define o tipo de mídia para o exemplo. Esse método implementa o método IMediaSample:: SetMediaType.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Método CMediaSample. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e7059e0d9b2d91b6a938c67445f185a2c9be0daf5831c30b235918ab7820b1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832166"
---
# <a name="cmediasamplesetmediatype-method"></a>Método CMediaSample. SetMediaType

O `SetMediaType` método define o tipo de mídia para o exemplo. Esse método implementa o método [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/> |



 

## <a name="remarks"></a>Comentários

Esse método define a variável de membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) , que especifica o tipo de mídia e a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica se o tipo de mídia foi alterado.

Esse método faz uma cópia da estrutura do \_ tipo de mídia am \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




