---
description: O método Exit sinaliza o thread de streaming para sair.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Método CSourceStream. Exit (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2c1c0de67eaa1067a4c72f3500674dddef65ddbb11af1b520973120d2df3c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687426"
---
# <a name="csourcestreamexit-method"></a>Método CSourceStream. Exit

O `Exit` método sinaliza o thread de streaming para sair.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Exit();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ inesperado.

## <a name="remarks"></a>Comentários

O método [**CSourceStream:: Inactive**](csourcestream-inactive.md) chama esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




