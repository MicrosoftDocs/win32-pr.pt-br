---
description: O identificador do thread que chamou pela última vez o método IPinFlowControl::Block nesse pino. Essa variável de membro só é válida enquanto o pin está bloqueado.
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: Membro CDynamicOutputPin::m_dwBlockCallerThreadID (Amfilter.h)
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
ms.openlocfilehash: b52bd7f718798ea9dd2cf9d227f6d22e069d2c1a59bb8591f6126c20599af9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539746"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Membro CDynamicOutputPin::m \_ dwBlockCallerThreadID

O identificador do thread que chamou pela última vez [**o método IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) nesse pino. Essa variável de membro só é válida enquanto o pin está bloqueado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Comentários

Antes de acessar essa variável, mantenha a [**seção crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




