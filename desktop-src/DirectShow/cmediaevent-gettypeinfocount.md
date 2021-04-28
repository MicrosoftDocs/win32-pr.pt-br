---
description: Método CMediaEvent. GetTypeInfoCount – recupera o número de interfaces de informações de tipo fornecidas por um objeto.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Método CMediaEvent. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099114"
---
# <a name="cmediaeventgettypeinfocount-method"></a>Método CMediaEvent. GetTypeInfoCount

Recupera o número de interfaces de informações de tipo fornecidas por um objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pctinfo* 
</dt> <dd>

Ponteiro para o número de interfaces de informações de tipo que o objeto fornece. Se o objeto fornecer informações de tipo, esse número será 1; caso contrário, o número será 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o \_ ponteiro E se *pctinfo* for inválido; caso contrário, retornará S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




