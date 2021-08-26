---
description: O método SetWaiting incrementa a contagem de threads em espera.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Método CBaseAllocator.SetWaiting (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 674528b6da53b7835e437afac9a0564f91785b2f9a13f132e87a6763b80881c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057456"
---
# <a name="cbaseallocatorsetwaiting-method"></a>Método CBaseAllocator.SetWaiting

O `SetWaiting` método incrementa a contagem de threads em espera.

## <a name="syntax"></a>Sintaxe


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método incrementa a variável de membro [**CBaseAllocator::m \_ lWaiting.**](cbaseallocator-m-lwaiting.md) Se um thread estiver bloqueado no método [**CBaseAllocator::GetBuffer,**](cbaseallocator-getbuffer.md) o alocador chamará e aguardará que o semáforo `SetWaiting` [**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md) seja sinalizado. O [**método CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) sinaliza o semáforo e define *m \_ lWaiting* de volta para zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




