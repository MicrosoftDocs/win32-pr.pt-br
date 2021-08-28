---
description: O método Invoke fornece acesso a métodos e propriedades expostas por um objeto.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Método CDeferredCommand. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1df087e71ba03ef67ea250235a4ef8a9ef5e6623efe67594381111de6088cf7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074370"
---
# <a name="cdeferredcommandinvoke-method"></a>Método CDeferredCommand. Invoke

O `Invoke` método fornece acesso a métodos e propriedades expostas por um objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará VFW \_ E \_ já \_ cancelado se **m \_ pQueue** for **nulo**. Caso contrário, retorna o **HRESULT** resultante de uma chamada para **IDispatch:: GetTypeInfo** ou **IUnknown:: QueryInterface**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




