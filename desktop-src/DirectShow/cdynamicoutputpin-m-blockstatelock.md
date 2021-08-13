---
description: Seção crítica que protege o estado de bloqueio.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Membro CDynamicOutputPin:: m_BlockStateLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa5382a30dcd434965c53e893d6818ab0f08a84c19ea0ddec53846c0c01c80f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656676"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a>Membro de CDynamicOutputPin:: m \_ BlockStateLock

Seção crítica que protege o estado de bloqueio.

## <a name="syntax"></a>Sintaxe


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a>Comentários

Mantenha esta seção crítica antes de usar qualquer uma das seguintes variáveis de membro:

-   [**CDynamicOutputPin:: m \_ blockstate**](cdynamicoutputpin-m-blockstate.md)
-   [**CDynamicOutputPin:: m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [**CDynamicOutputPin:: m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [**CDynamicOutputPin:: m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




