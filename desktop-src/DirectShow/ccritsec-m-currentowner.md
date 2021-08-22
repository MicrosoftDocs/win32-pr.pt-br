---
description: Identificador de thread do thread de propriedade.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: Membro CCritSec::m_currentOwner (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71c88055f5068a5486c1eb6e3ac739235a6b7cde2e8d6b767380160ff12503be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657209"
---
# <a name="ccritsecm_currentowner-member"></a>Membro CCritSec::m \_ currentOwner

Identificador de thread do thread de propriedade.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Comentários

Essa variável de membro é definida apenas na versão de depuração da classe base. As [Funções críticas de depuração de seção](critical-section-debugging-functions.md) usam esse membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




