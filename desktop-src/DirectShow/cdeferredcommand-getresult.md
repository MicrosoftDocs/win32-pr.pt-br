---
description: O método GetResult recupera a lista de argumentos resultantes, se houver.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: Método CDeferredCommand. GetResult (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811744"
---
# <a name="cdeferredcommandgetresult-method"></a>Método CDeferredCommand. GetResult

O `GetResult` método recupera a lista de argumentos resultantes, se houver.

## <a name="syntax"></a>Sintaxe


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para uma **variante** que contém a lista de argumentos do método, se existir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




