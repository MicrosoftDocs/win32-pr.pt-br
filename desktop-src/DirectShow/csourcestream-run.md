---
description: O método Run sinaliza o thread de streaming para execução.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Método CSourceStream. Run (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779547"
---
# <a name="csourcestreamrun-method"></a>Método CSourceStream. Run

O `Run` método sinaliza o thread de streaming a ser executado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou E \_ inesperado.

## <a name="remarks"></a>Comentários

Na classe base, esse método tem o mesmo efeito que a solicitação [**CSourceStream::P ause**](csourcestream-pause.md) e não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




