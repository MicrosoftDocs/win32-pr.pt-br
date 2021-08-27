---
description: Método CBasePin.SetMediaType – o método SetMediaType define o tipo de mídia para a conexão.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin.SetMediaType (Amfilter.h)
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
ms.openlocfilehash: e71047b5063a5975266e5e24db936a0baf9e7b65e81ce29b402ccce4638267a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108636"
---
# <a name="cbasepinsetmediatype-method"></a>Método CBasePin.SetMediaType

O `SetMediaType` método define o tipo de mídia para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método estabelece o formato de uma conexão de pino. Antes de chamar esse método, o pin chama o [**método CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) para determinar se o tipo de mídia é aceitável. Portanto, o *parâmetro pmt* é presumido como um tipo de mídia aceitável.

Na classe base, esse método define a variável de membro [**CBasePin::mt \_**](cbasepin-m-mt.md) e retorna S \_ OK. Uma classe derivada poderá substituir esse método se exigir notificação quando o tipo de mídia for definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




