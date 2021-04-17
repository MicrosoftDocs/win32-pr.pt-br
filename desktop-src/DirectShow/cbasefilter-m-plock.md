---
description: Ponteiro para uma seção crítica que é usada para serializar alterações de estado.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Membro CBaseFilter:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752910"
---
# <a name="cbasefilterm_plock-member"></a>Membro de CBaseFilter:: m \_ pLock

Ponteiro para uma seção crítica que é usada para serializar alterações de estado.

## <a name="syntax"></a>Sintaxe


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Comentários

Essa variável é inicializada no construtor da classe; consulte [**CBaseFilter:: CBaseFilter**](cbasefilter-cbasefilter.md).

Mantenha essa seção crítica durante as transições de estado ou quando um método acessar o estado em várias operações. A classe base contém a seção crítica nos seguintes métodos:

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter:: getsync**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter:: IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter:: setsincronizate**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter:: Run**](cbasefilter-run.md)
-   [**CBaseFilter:: Stop**](cbasefilter-stop.md)

Não mantenha esta seção crítica durante operações de streaming (isto é, ao entregar amostras a um filtro downstream). Serialize operações de streaming usando uma seção crítica diferente. Caso contrário, isso pode causar deadlock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> <dt>

[Threads e seções críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 




