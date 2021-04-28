---
description: Método CBasePin. SetMediaType – o método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095975"
---
# <a name="cbasepinsetmediatype-method"></a>Método CBasePin. SetMediaType

O `SetMediaType` método define o tipo de mídia para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método estabelece o formato para uma conexão de PIN. Antes de chamar esse método, o PIN chama o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar se o tipo de mídia é aceitável. Portanto, o parâmetro *PGTO* é considerado um tipo de mídia aceitável.

Na classe base, esse método define a variável de membro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) e retorna S \_ OK. Uma classe derivada pode substituir esse método se precisar de notificação quando o tipo de mídia estiver definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




