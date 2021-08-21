---
description: Sinalizador para substituir o processamento em lotes. Definir esse sinalizador como TRUE substitui o sinalizador COutputQueue::m bBatchExact e fornece todos \_ os exemplos pendentes.
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: Membro COutputQueue::m_bSendAnyway (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c01ec87fb8e1d9b33fd88806b0d2798e2b13e76eea2ec47b4e1766a7e10201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954145"
---
# <a name="coutputqueuem_bsendanyway-member"></a>Membro COutputQueue::m \_ bSendAnyway

Sinalizador para substituir o processamento em lotes. Definir esse sinalizador como **TRUE** substitui o [**sinalizador COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) e fornece todos os exemplos pendentes.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




