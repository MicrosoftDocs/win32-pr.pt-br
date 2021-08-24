---
description: O método Stop interrompe o objeto . Esse método implementa o método IMediaFilter::Stop.
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Método CBaseMediaFilter.Stop (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: effe2df53508cd9c1f6523356eb7296458208c3ee0e61c1dd12c94bd87b6ad31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793226"
---
# <a name="cbasemediafilterstop-method"></a>Método CBaseMediaFilter.Stop

O `Stop` método interrompe o objeto . Esse método implementa o [**método IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Na classe base, esse método define a variável membro de estado [**CBaseMediaFilter::m \_**](cbasemediafilter-m-state.md) como State \_ Stopped, mas não faz mais nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




