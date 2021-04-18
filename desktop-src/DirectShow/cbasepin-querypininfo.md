---
description: 'O método QueryPinInfo recupera informações sobre o PIN. Esse método implementa o método IPin:: QueryPinInfo.'
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Método CBasePin. QueryPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f69977a15deb7d84b3370bb6e08c02a4e5129212
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749257"
---
# <a name="cbasepinquerypininfo-method"></a>Método CBasePin. QueryPinInfo

O `QueryPinInfo` método recupera informações sobre o PIN. Esse método implementa o método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInfo* 
</dt> <dd>

Ponteiro para uma estrutura de [**\_ informações de PIN**](/windows/win32/api/strmif/ns-strmif-pin_info) que recebe as informações de PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou o \_ ponteiro.

## <a name="remarks"></a>Comentários

Esse método usa a variável de membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) para o membro **achName** da estrutura de informações de PIN \_ .

Quando o método retornar, se o membro **pFilter** da estrutura de \_ informações de PIN for não **nulo**, ele terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




