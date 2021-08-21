---
description: O método ThrottleWait insere um período de espera após cada quadro.
ms.assetid: 69306093-f5db-4170-b30f-e33cfa448e9f
title: Método CBaseVideoRenderer. ThrottleWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ThrottleWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d61c0e934208ad72e678595ce668c6c7ff72eda3371c792b294df9f2d5915612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954745"
---
# <a name="cbasevideorendererthrottlewait-method"></a>Método CBaseVideoRenderer. ThrottleWait

O `ThrottleWait` método insere um período de espera após cada quadro.

## <a name="syntax"></a>Sintaxe


```C++
void ThrottleWait();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro aguarda um período de tempo obtido do membro de dados **m \_ trThrottle** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




