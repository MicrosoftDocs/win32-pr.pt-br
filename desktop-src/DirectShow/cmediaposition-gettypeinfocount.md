---
description: Método CMediaPosition. GetTypeInfoCount – o método GetTypeInfoCount recupera o número de interfaces de informações de tipo que o objeto fornece.
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Método CMediaPosition. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 032584025d91d6e21b02ed74b26b2e59d55e3a6e044c215d586913d8417a412e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157004"
---
# <a name="cmediapositiongettypeinfocount-method"></a>Método CMediaPosition. GetTypeInfoCount

O `GetTypeInfoCount` método recupera o número de interfaces de informações de tipo que o objeto fornece.

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

Ponteiro para uma variável que recebe o número de interfaces de informações de tipo fornecidas pelo objeto. Quando o método retorna, o valor é 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                               | Descrição                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaPosition**](cmediaposition.md)
</dt> </dl>

 

 




