---
description: Duração do fluxo. Por padrão, o valor é definido como o valor da variável de membro CSourceSeeking::m \_ rtStop.
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: Membro CSourceSeeking::m_rtDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6aa62a3cdf906a4e9666b7786c08e49fca250ef042d187902132410cc2f0abaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053966"
---
# <a name="csourceseekingm_rtduration-member"></a>Membro CSourceSeeking::m \_ rtDuration

Duração do fluxo. Por padrão, o valor é definido como o valor da variável de membro [**CSourceSeeking::m \_ rtStop.**](csourceseeking-m-rtstop.md)

## <a name="syntax"></a>Sintaxe


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Comentários

Mantenha a **seção \_ crítica m pLock** antes de acessar essa variável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




