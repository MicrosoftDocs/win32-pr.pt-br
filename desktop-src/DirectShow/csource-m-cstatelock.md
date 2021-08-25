---
description: Objeto de seção crítico que protege o estado do filtro. O método auxiliar CSource::p StateLock retorna um ponteiro para essa variável de membro.
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: Membro CSource::m_cStateLock (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de77935fd71f0b82f3cfe1f70dae3879c97bd86b4ca6b802efd46dd42730288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915306"
---
# <a name="csourcem_cstatelock-member"></a>Membro CSource::m \_ cStateLock

Objeto de seção crítico que protege o estado do filtro. O [**método auxiliar CSource::p StateLock**](csource--pstatelock.md) retorna um ponteiro para essa variável de membro.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




