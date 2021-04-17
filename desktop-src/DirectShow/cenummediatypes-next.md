---
description: 'O método Next recupera um número especificado de tipos de mídia. Esse método implementa o método IEnumMediaTypes:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Método CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751246"
---
# <a name="cenummediatypesnext-method"></a>Método CEnumMediaTypes. Next

O `Next` método recupera um número especificado de tipos de mídia. Esse método implementa o método [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Número de tipos de mídia a serem recuperados.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Matriz de ponteiros para as estruturas de [**\_ \_ tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type) , de tamanho *cPins*.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Ponteiro para uma variável que recebe o número de tipos de mídia que o método retornou. Pode ser **NULL** se *cMediaTypes* for 1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                    | Não foi possível recuperar quantos tipos de mídia solicitados.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento inválido.<br/>                                                        |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Argumento de ponteiro **nulo** .<br/>                                               |
| <dl> <dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt> </dl> | O estado do PIN foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="remarks"></a>Comentários

Se o método tiver sucesso, a matriz especificada por *ppMediaTypes* conterá ponteiros para \_ estruturas de tipo de mídia am \_ . O número de estruturas é igual a *\* pcFetched*. Libere cada tipo de mídia chamando a função [**DeleteMediaType**](deletemediatype.md) .

Esse método chama o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) do PIN para recuperar os tipos de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




