---
description: O método IsIdle determina se o objeto está aguardando dados.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: Método COutputQueue. IsIdle (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c231e6e9dac3e05be6c01a2f3ebd87b5cdd69b8822a5ce26f930277c457206c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652116"
---
# <a name="coutputqueueisidle-method"></a>Método COutputQueue. IsIdle

O `IsIdle` método determina se o objeto está aguardando dados.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsIdle();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se o thread estiver aguardando e a matriz de exemplo estiver vazia. Caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




