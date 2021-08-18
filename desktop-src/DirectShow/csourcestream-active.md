---
description: 'O método ativo notifica o PIN de que o filtro está ativo agora. Esse método substitui o método CBasePin:: active. Se o PIN estiver conectado, esse método iniciará o thread de streaming.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Método CSourceStream. Active (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 427c0318bad4df810b29f3596e3a9516f8dbb73e97dd7e378c561bef28bf2f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073331"
---
# <a name="csourcestreamactive-method"></a>Método CSourceStream. active

O `Active` método notifica o PIN de que o filtro está ativo agora. Esse método substitui o método [**CBasePin:: active**](cbasepin-active.md) . Se o PIN estiver conectado, esse método iniciará o thread de streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                             | Descrição                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O PIN já está ativo.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                    |
| <dl> <dt>**E \_ falha**</dt> </dl>  | Não foi possível iniciar o thread.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




