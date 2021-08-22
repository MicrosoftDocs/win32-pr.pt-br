---
description: O método Stop sinaliza o thread de streaming para parar.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Método CSourceStream. Stop (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ac5eb7d6b066920210d4f955084afa46ddc71d1c17820fe0300acc66b53bb8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073160"
---
# <a name="csourcestreamstop-method"></a>Método CSourceStream. Stop

O `Stop` método sinaliza o thread de streaming para parar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ inesperado.

## <a name="remarks"></a>Comentários

O método [**CSourceStream:: Inactive**](csourcestream-inactive.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




