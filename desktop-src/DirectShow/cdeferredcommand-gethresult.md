---
description: O método gethresult recupera o valor HRESULT do comando invocado.
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: Método CDeferredCommand. gethresult (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811745"
---
# <a name="cdeferredcommandgethresult-method"></a>Método CDeferredCommand. gethresult

O `GetHResult` método recupera o valor **HRESULT** do comando chamado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phrResult* 
</dt> <dd>

Ponteiro para o valor **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna E \_ Abort se **m \_ pQueue** for **nulo**. Caso contrário, retornará S \_ OK.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IDeferredCommand:: gethresult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




