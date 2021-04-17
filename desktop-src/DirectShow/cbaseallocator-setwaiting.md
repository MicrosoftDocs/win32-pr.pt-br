---
description: O método setaguardando incrementa a contagem de threads em espera.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Método CBaseAllocator. setaguardating (Amfilter. h)
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
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752918"
---
# <a name="cbaseallocatorsetwaiting-method"></a>Método CBaseAllocator. setaguardando

O `SetWaiting` método incrementa a contagem de threads em espera.

## <a name="syntax"></a>Sintaxe


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método incrementa a variável de membro [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) . Se um thread estiver bloqueado no método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) , o alocador chamará `SetWaiting` e esperará que o semáforo de [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) seja sinalizado. O método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) sinaliza o semáforo e define *m \_ lWaiting* de volta como zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




