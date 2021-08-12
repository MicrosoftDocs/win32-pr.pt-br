---
description: Método CBaseDispatch.GetTypeInfoCount – o método GetTypeInfoCount recupera o número de interfaces de informações de tipo que o objeto fornece.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Método CBaseDispatch.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da80cdb4810ea3e598ad9483ccf52e8033ccb1a5b7ee65351e2cfcc273a3415f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660013"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>Método CBaseDispatch.GetTypeInfoCount

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

Ponteiro para uma variável que recebe o número de interfaces de informações de tipo fornecidas pelo objeto . Quando o método retorna, o valor é 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                               | Descrição                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                   |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | Argumento de ponteiro **NULL.**<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseDispatch**](cbasedispatch.md)
</dt> </dl>

 

 




