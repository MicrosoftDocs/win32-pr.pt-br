---
description: Método de construtor.
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
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751693"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

