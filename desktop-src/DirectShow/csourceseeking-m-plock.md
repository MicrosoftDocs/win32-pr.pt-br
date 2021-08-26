---
description: Ponteiro para um objeto de seção crítico.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: Membro CSourceSeeking::m_pLock (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f230fcaee4ebb59520319d5dfd7cf8295ce8721716cd1ffb02b534e242bd99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054016"
---
# <a name="csourceseekingm_plock-member"></a>Membro CSourceSeeking::m \_ pLock

Ponteiro para um objeto de seção crítico. A classe usa esta seção crítica para sincronizar o acesso às horas de início e de `CSourceSeeking` parada, duração e variáveis de taxa. Essa variável é inicializada no método do construtor; consulte [**CSourceSeeking::CSourceSeeking.**](csourceseeking-csourceseeking.md)

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




