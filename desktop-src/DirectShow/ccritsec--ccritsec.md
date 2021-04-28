---
description: CCritSec. ~ CCritSec destruidor-método Destruitor.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec Destruitor (Wxutil. h)
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
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095804"
---
# <a name="ccritsecccritsec-destructor"></a>Destruidor CCritSec. ~ CCritSec

Método destruidor.

## <a name="syntax"></a>Sintaxe


```C++
~CCritSec();
```



## <a name="remarks"></a>Comentários

Esse método chama a função [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para excluir a seção crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

