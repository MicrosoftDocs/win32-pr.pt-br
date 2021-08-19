---
description: O método QueryPinInfo recupera informações sobre o pino. Esse método implementa o método IPin::QueryPinInfo.
ms.assetid: 9de41f61-9f03-4594-a320-2f7f0ed734fd
title: Método CBasePin.QueryPinInfo (Amfilter.h)
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
ms.openlocfilehash: 544039b1076848cb796f290ea98aa8aac359b26ebfb64f90a27d316a9d0cc34f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823220"
---
# <a name="cbasepinquerypininfo-method"></a>Método CBasePin.QueryPinInfo

O `QueryPinInfo` método recupera informações sobre o pino. Esse método implementa o [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryPinInfo(
   PIN_INFO *pInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pinfo* 
</dt> <dd>

Ponteiro para uma [**estrutura \_ PIN INFO**](/windows/win32/api/strmif/ns-strmif-pin_info) que recebe as informações de pin.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ POINTER.

## <a name="remarks"></a>Comentários

Esse método usa a [**variável de membro CBasePin::m \_ pName**](cbasepin-m-pname.md) para **o membro achName** da estrutura PIN \_ INFO.

Quando o método retorna, se o **membro pFilter** da estrutura PIN INFO for não \_ **NULL,** ele terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




