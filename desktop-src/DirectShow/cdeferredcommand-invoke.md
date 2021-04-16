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
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759144"
---
# <a name="cdeferredcommandinvoke-method"></a>Método CDeferredCommand. Invoke

O `Invoke` método fornece acesso a métodos e propriedades expostas por um objeto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Invoke();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará VFW \_ E \_ já \_ cancelado se **m \_ pQueue** for **nulo**. Caso contrário, retorna o **HRESULT** resultante de uma chamada para **IDispatch:: GetTypeInfo** ou **IUnknown:: QueryInterface**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




