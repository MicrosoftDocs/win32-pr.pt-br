---
description: Recupera o número de interfaces de informações de tipo fornecidas por um objeto.
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
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775637"
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

## <a name="return-value"></a>Retornar valor

Retorna o \_ ponteiro E se *pctinfo* for inválido; caso contrário, retornará S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




