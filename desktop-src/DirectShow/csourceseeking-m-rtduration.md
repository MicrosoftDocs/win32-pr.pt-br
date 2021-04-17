---
description: 'Duração do fluxo. Por padrão, o valor é definido como o valor da variável de membro CSourceSeeking:: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Membro CSourceSeeking:: m_rtDuration (Ctlutil. h)'
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
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748620"
---
# <a name="csourceseekingm_rtduration-member"></a>Membro de CSourceSeeking:: m \_ rtDuration

Duração do fluxo. Por padrão, o valor é definido como o valor da variável de membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="syntax"></a>Sintaxe


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Comentários

Mantenha a seção crítica **m \_ pLock** antes de acessar essa variável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




