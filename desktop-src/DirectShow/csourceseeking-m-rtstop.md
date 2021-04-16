---
description: Hora de parada. Por padrão, o valor é definido como um número muito grande. A classe derivada pode redefinir o valor em seu construtor ou quando o filtro é inicializado.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Membro CSourceSeeking:: m_rtStop (Ctlutil. h)'
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
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751240"
---
# <a name="csourceseekingm_rtstop-member"></a>Membro de CSourceSeeking:: m \_ rtStop

Hora de parada. Por padrão, o valor é definido como um número muito grande. A classe derivada pode redefinir o valor em seu construtor ou quando o filtro é inicializado.

## <a name="syntax"></a>Sintaxe


```C++
CRefTime m_rtStop;
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

 

 




