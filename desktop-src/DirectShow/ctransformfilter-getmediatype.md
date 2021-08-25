---
description: Método CTransformFilter.GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial para o pino de saída.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Método CTransformFilter.GetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b471ac42ceb44f5e65a2ac08365bf97ab0e3157816b772b331cde0fa0b13bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907526"
---
# <a name="ctransformfiltergetmediatype-method"></a>Método CTransformFilter.GetMediaType

O `GetMediaType` método recupera um tipo de mídia preferencial para o pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPosition* 
</dt> <dd>

Valor de índice baseado em zero.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                            | Descrição                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>              |
| <dl> <dt>**VFW \_ NÃO TEM MAIS \_ \_ \_ ITENS**</dt> </dl> | Índice fora do intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que zero.<br/> |



 

## <a name="remarks"></a>Comentários

O método [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) do pino de saída chama esse método. A classe derivada deve implementar esse método. Para obter mais informações, [**consulte CBasePin::GetMediaType**](cbasepin-getmediatype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




