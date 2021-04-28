---
description: Método CTransformOutputPin. GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial, por valor de índice.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Método CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094894"
---
# <a name="ctransformoutputpingetmediatype-method"></a>Método CTransformOutputPin. GetMediaType

O `GetMediaType` método recupera um tipo de mídia preferencial, por valor de índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice baseado em zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                            | Descrição                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito<br/>            |
| <dl> <dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt> </dl> | Índice fora do intervalo<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) . Se o pino de entrada do filtro não estiver conectado, o método retornará VFW \_ s \_ não \_ mais \_ itens. Caso contrário, ele chama o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) do filtro para recuperar o tipo de mídia. O método **CTransformFilter:: GetMediaType** é virtual puro; a classe derivada do filtro deve substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




