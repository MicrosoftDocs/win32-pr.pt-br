---
description: Construtor de CCritSec. CCritSec-método de construtor.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Construtor CCritSec. CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119794"
---
# <a name="ccritsecccritsec-constructor"></a>Construtor CCritSec. CCritSec

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CCritSec();
```



## <a name="parameters"></a>Parâmetros

Este construtor não tem parâmetros.

## <a name="remarks"></a>Comentários

Esse método chama a função [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) para inicializar a seção crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

