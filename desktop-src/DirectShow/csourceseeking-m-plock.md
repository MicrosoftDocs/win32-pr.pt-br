---
description: Ponteiro para um objeto de seção crítica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Membro CSourceSeeking:: m_pLock (Ctlutil. h)'
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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758070"
---
# <a name="csourceseekingm_plock-member"></a>Membro de CSourceSeeking:: m \_ pLock

Ponteiro para um objeto de seção crítica. A `CSourceSeeking` classe usa essa seção crítica para sincronizar o acesso às horas de início e parada, à duração e às variáveis de taxa. Essa variável é inicializada no método do Construtor; consulte [**CSourceSeeking:: CSourceSeeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




