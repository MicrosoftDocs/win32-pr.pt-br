---
description: 'O identificador do thread que chamou por último o método IPinFlowControl:: Block neste PIN. Esta variável de membro só é válida enquanto o PIN está bloqueado.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Membro CDynamicOutputPin:: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750049"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Membro de CDynamicOutputPin:: m \_ dwBlockCallerThreadID

O identificador do thread que chamou por último o método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) neste PIN. Esta variável de membro só é válida enquanto o PIN está bloqueado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Comentários

Antes de acessar essa variável, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




