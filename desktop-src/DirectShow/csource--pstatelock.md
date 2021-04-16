---
description: O método pStateLock recupera um ponteiro para o objeto de seção crítica do filtro.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: Método CSource. pStateLock (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757897"
---
# <a name="csourcepstatelock-method"></a>Método CSource. pStateLock

O método **pStateLock** recupera um ponteiro para o objeto de seção crítica do filtro.

> [!Note]  
> Embora nomeado como uma variável de membro, **pStateLock** é um método.

 

## <a name="syntax"></a>Sintaxe


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a variável de membro [**CSource:: m \_ cStateLock**](csource-m-cstatelock.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




