---
description: Valor booliana que especifica se esse bloqueio deve ser rastreado.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: Membro CCritSec::m_fTrace (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5a47437e4f9ab475b64979ec970604ac7a621d2ab53ea7a3c87742fa81a8aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074390"
---
# <a name="ccritsecm_ftrace-member"></a>Membro CCritSec::m \_ fTrace

Valor booliana que especifica se esse bloqueio deve ser rastreado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Comentários

Essa variável de membro é definida apenas na versão de depuração da classe base. Se o valor for **TRUE,** um rastreamento do estado de bloqueio será gravado no log de depuração. (O log de depuração para seções críticas deve estar ativo.) Para obter mais informações, consulte [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




