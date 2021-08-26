---
description: Método CBasePin.GetMediaType – o método GetMediaType recupera um tipo de mídia preferencial, por valor de índice.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Método CBasePin.GetMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc202c3b6dbc570d063ef74619b266c2faa20cb74322b29e61626418412e2cb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044076"
---
# <a name="cbasepingetmediatype-method"></a>Método CBasePin.GetMediaType

O `GetMediaType` método recupera um tipo de mídia preferencial, por valor de índice.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMediaType(
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

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que recebe o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles na tabela a seguir.



| Código de retorno                                                                                            | Descrição                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>              |
| <dl> <dt>**VFW \_ NÃO TEM MAIS \_ \_ \_ ITENS**</dt> </dl> | Índice fora do intervalo.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Índice menor que zero.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Erro inesperado.<br/>     |



 

## <a name="remarks"></a>Comentários

Na lista do pin de tipos de mídia preferenciais, esse método retorna o tipo com um valor de índice *de iPosition*. A [**classe CEnumMediaTypes**](cenummediatypes.md) chama esse método para enumerar tipos de mídia preferenciais.

A classe base retorna E \_ UNEXPECTED. Substitua esse método em sua classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




