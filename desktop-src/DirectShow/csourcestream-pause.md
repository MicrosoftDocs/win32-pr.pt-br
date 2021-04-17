---
description: O método pause sinaliza o thread de streaming para se tornar ativo.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Método CSourceStream. PAUSE (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759560"
---
# <a name="csourcestreampause-method"></a>Método CSourceStream. Pause

O `Pause` método sinaliza o thread de streaming para se tornar ativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou E \_ inesperado.

## <a name="remarks"></a>Comentários

O método [**CSourceStream:: active**](csourcestream-active.md) chama esse método. Quando o método [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) recebe essa solicitação, ele chama o método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




