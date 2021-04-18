---
description: 'Evento opcional sinalizado sempre que o objeto remove um exemplo da fila. O valor é inicialmente nulo. Chame o método COutputQueue:: SetPopEvent para especificar um identificador de evento.'
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Membro COutputQueue:: m_hEventPop (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759308"
---
# <a name="coutputqueuem_heventpop-member"></a>Membro de COutputQueue:: m \_ hEventPop

Evento opcional sinalizado sempre que o objeto remove um exemplo da fila. O valor é inicialmente **nulo**. Chame o método [**COutputQueue:: SetPopEvent**](coutputqueue-setpopevent.md) para especificar um identificador de evento.

## <a name="syntax"></a>Syntax


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




