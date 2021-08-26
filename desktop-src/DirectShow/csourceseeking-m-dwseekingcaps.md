---
description: Buscando recursos.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: Membro CSourceSeeking::m_dwSeekingCaps (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98044f8a05c22022f66e6014be591d99ec57451e33e8f2d7d464e6793bec19e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054026"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Membro CSourceSeeking::m \_ dwSeekingCaps

Buscando recursos.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Comentários

Por padrão, o valor é definido como a combinação bit a bit dos seguintes sinalizadores:

-   AM \_ SEEKING \_ CanSeekForwards
-   AM \_ SEEKING \_ CanSeekBackwards
-   AM \_ SEEKING \_ CanSeekAbsolute
-   AM \_ SEEKING \_ CanGetStopPos
-   AM \_ SEEKING \_ CanGetDuration

Se o filtro for compatível com um conjunto diferente de funcionalidades, substitua esse valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




