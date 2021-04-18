---
description: O método NotifySample libera todos os threads que estão aguardando exemplos.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Método CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780893"
---
# <a name="cbaseallocatornotifysample-method"></a>Método CBaseAllocator. NotifySample

O `NotifySample` método libera todos os threads que estão aguardando exemplos.

## <a name="syntax"></a>Sintaxe


```C++
void NotifySample();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando há threads aguardando exemplos, o valor de [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) é maior que zero. Se *m \_ lWaiting* for maior que zero, esse método chamará a função **ReleaseSemaphore** no semáforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) , ativando todos os threads em espera. Ele também redefine *m \_ lWaiting* para zero.

Esse método é chamado de dentro do método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , quando um exemplo é retornado para a lista livre; e do método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , quando o alocador é decommitdo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




