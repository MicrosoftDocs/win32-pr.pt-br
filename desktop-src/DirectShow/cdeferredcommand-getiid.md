---
description: O método GetIID Recupera o identificador de interface (IID) da interface na qual o método será executado.
ms.assetid: d6eb7d46-294a-4169-96d3-4bed02c48c08
title: Método CDeferredCommand. GetIID (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetIID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c5d43f04d8331f39e46e3223a64c09ad306585a1e29fd7627a0f50159d74cde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910075"
---
# <a name="cdeferredcommandgetiid-method"></a>Método CDeferredCommand. GetIID

O `GetIID` método recupera o identificador de interface (IID) da interface na qual o método será executado.

## <a name="syntax"></a>Sintaxe


```C++
REFIID GetIID();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o IID da interface na qual o método será executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




