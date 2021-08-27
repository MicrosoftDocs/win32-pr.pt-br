---
description: Hora de parada. Por padrão, o valor é definido como um número muito grande. A classe derivada pode redefinir o valor em seu construtor ou quando o filtro é inicializado.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: Membro CSourceSeeking::m_rtStop (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4408fddf42070012aa6e1eb3a0268e8e449b571828c0904524f3cc8d27df3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102996"
---
# <a name="csourceseekingm_rtstop-member"></a>Membro CSourceSeeking::m \_ rtStop

Hora de parada. Por padrão, o valor é definido como um número muito grande. A classe derivada pode redefinir o valor em seu construtor ou quando o filtro é inicializado.

## <a name="syntax"></a>Sintaxe


```C++
CRefTime m_rtStop;
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

 

 




