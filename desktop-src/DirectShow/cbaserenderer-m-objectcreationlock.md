---
description: Bloquear para proteger a criação de objetos dentro do filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Membro CBaseRenderer:: m_ObjectCreationLock (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b0925aab0345d5eed8da19e12f355c417d66c1f36a1384a05950a87d4c95b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429306"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>Membro de CBaseRenderer:: m \_ ObjectCreationLock

Bloquear para proteger a criação de objetos dentro do filtro. O filtro mantém esse bloqueio quando cria o pino de entrada ([**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) ou o objeto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md)). Esse bloqueio impede que vários threads tentem criar um desses objetos ao mesmo tempo.

## <a name="syntax"></a>Sintaxe


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




