---
description: Método CBasePin. CheckMediaType – o método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Método CBasePin. CheckMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099393"
---
# <a name="cbasepincheckmediatype-method"></a>Método CBasePin. CheckMediaType

O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o tipo de mídia proposto for aceitável. Caso contrário, retorna S \_ false ou um código de erro.

## <a name="remarks"></a>Comentários

A classe derivada deve substituir esse método virtual puro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




