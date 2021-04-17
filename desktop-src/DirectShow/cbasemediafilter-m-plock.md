---
description: Ponteiro para uma seção crítica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Membro CBaseMediaFilter:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752906"
---
# <a name="cbasemediafilterm_plock-member"></a>Membro de CBaseMediaFilter:: m \_ pLock

Ponteiro para uma seção crítica.

## <a name="syntax"></a>Sintaxe


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Comentários

A seção crítica é mantida durante as transições de estado ([**CBaseMediaFilter:: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter:: Stop**](cbasemediafilter-stop.md)), ao acessar o relógio de referência ([**CBaseMediaFilter:: setsyncname**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: getsyncname**](cbasemediafilter-getsyncsource.md)) e no método [**CBaseMediaFilter:: IsActive**](cbasemediafilter-isactive.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




