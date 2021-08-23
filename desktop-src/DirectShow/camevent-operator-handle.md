---
description: Recupera o identificador de evento. Não há suporte para esse operador como um L-Value.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Método de identificador CAMEvent. Operator (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afc3bcc1044d3d14b7ebf77ce12027fb3b772185f62b917fce7b74fbb3fa7e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689326"
---
# <a name="cameventoperator-handle-method"></a>Método de identificador CAMEvent. Operator

Recupera o identificador de evento. Não há suporte para esse operador como um L-Value.

## <a name="syntax"></a>Sintaxe


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a variável de membro [**CAMEvent:: m \_ hEvent**](camevent-m-hevent.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMEvent**](camevent.md)
</dt> </dl>

 

 




