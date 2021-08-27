---
description: Sinalizador que indica se o retorno de chamada de versão está habilitado. Esse sinalizador é definido no método do construtor. Se o valor for FALSE, chamar o método CBaseAllocator::SetNotify faz com que uma declaração seja a incêndio (em builds de depuração).
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: Membro CBaseAllocator::m_fEnableReleaseCallback (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2fc1dfebb051ddffffce341547562901153b47bd5da002ebd847965593a73d93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131456"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>Membro CBaseAllocator::m \_ fEnableReleaseCallback

Sinalizador que indica se o retorno de chamada de versão está habilitado. Esse sinalizador é definido no método do construtor. Se o valor for **FALSE,** chamar o [**método CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) faz com que uma declaração seja a incêndio (em builds de depuração).

## <a name="syntax"></a>Syntax


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




