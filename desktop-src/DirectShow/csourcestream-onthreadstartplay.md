---
description: O método OnThreadStartPlay é chamado no início do método CSourceStream::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Método CSourceStream. OnThreadStartPlay (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcd1ccf4b507570e0219854d1f5044c1d95db63d04b8f9049449beb3941e95d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073170"
---
# <a name="csourcestreamonthreadstartplay-method"></a>Método CSourceStream. OnThreadStartPlay

O `OnThreadStartPlay` método é chamado no início do método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método não faz nada na classe base; Ele está disponível para a classe derivada substituir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




