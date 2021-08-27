---
description: O método Next recupera um número especificado de tipos de mídia. Esse método implementa o método IEnumMediaTypes::Next.
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Método CEnumMediaTypes.Next (Amfilter.h)
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
ms.openlocfilehash: f8dd593fe6ca550c55ffc1f769a303dd2d5cbf7a8d8c986be8a39278d7f334ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131286"
---
# <a name="cenummediatypesnext-method"></a>Método CEnumMediaTypes.Next

O `Next` método recupera um número especificado de tipos de mídia. Esse método implementa o [**método IEnumMediaTypes::Next.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next)

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

Número de tipos de mídia a recuperar.

</dd> <dt>

*ppMediaTypes* 
</dt> <dd>

Matriz de ponteiros para estruturas [**AM \_ MEDIA \_ TYPE,**](/windows/win32/api/strmif/ns-strmif-am_media_type) de *tamanho cPins*.

</dd> <dt>

*Pcfetched* 
</dt> <dd>

Ponteiro para uma variável que recebe o número de tipos de mídia retornados pelo método. Poderá ser **NULL** se *cMediaTypes* for 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Não foi recuperado tantos tipos de mídia quanto solicitado.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Argumento inválido.<br/>                                                        |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                  | Argumento de ponteiro **NULL.**<br/>                                               |
| <dl> <dt>**VFW \_ \_ ENUM \_ FORA DE \_ \_ SINCRONIA**</dt> </dl> | O estado do pino foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="remarks"></a>Comentários

Se o método for bem-sucedido, a matriz especificada por *ppMediaTypes* conterá ponteiros para estruturas AM \_ MEDIA \_ TYPE. O número de estruturas é igual a *\* pcFetched.* Liberar cada tipo de mídia chamando a [**função DeleteMediaType.**](deletemediatype.md)

Esse método chama o método [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) do pino para recuperar os tipos de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




