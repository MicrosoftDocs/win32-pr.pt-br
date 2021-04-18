---
description: Valor booliano que especifica se o bloqueio deve ser rastreado.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Membro CCritSec:: m_fTrace (Wxutil. h)'
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
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751898"
---
# <a name="ccritsecm_ftrace-member"></a>Membro de CCritSec:: m \_ fTrace

Valor booliano que especifica se o bloqueio deve ser rastreado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Comentários

Essa variável de membro é definida somente na versão de depuração da classe base. Se o valor for **true**, um rastreamento do estado de bloqueio será gravado no log de depuração. (O log de depuração para seções críticas deve estar ativo.) Para obter mais informações, consulte [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




