---
description: Destruidor CCritSec.~CCritSec – método destruidor.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Destruidor CCritSec.~CCritSec (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d34665bb18a6ea9f6e76ad6332a5d7f344993067848c1b5e473893e702b62a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999606"
---
# <a name="ccritsecccritsec-destructor"></a>Destruidor CCritSec.~CCritSec

Método destruidor.

## <a name="syntax"></a>Sintaxe


```C++
~CCritSec();
```



## <a name="remarks"></a>Comentários

Esse método chama a [**função DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para excluir a seção crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

