---
description: O método GetMediaType recupera um tipo de mídia preferencial, por valor de índice.
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
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758651"
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

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                            | Descrição                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Sucesso<br/>            |
| <dl> <dt>**VFW \_ S \_ não há \_ mais \_ itens**</dt> </dl> | Índice fora do intervalo<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) . Se o pino de entrada do filtro não estiver conectado, o método retornará VFW \_ s \_ não \_ mais \_ itens. Caso contrário, ele chama o método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) do filtro para recuperar o tipo de mídia. O método **CTransformFilter:: GetMediaType** é virtual puro; a classe derivada do filtro deve substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




