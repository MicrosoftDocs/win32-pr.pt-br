---
description: O método IsActive determina se o filtro está ativo no momento (em execução ou em pausa).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Método CBaseFilter. IsActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbbd9fedf94816d518ef9f8826542399d1d1e97f97137b2d86581d36c4a33e53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076636"
---
# <a name="cbasefilterisactive-method"></a>Método CBaseFilter. IsActive

O `IsActive` método determina se o filtro está ativo no momento (em execução ou em pausa).

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsActive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **true** se o filtro estiver em pausa ou em execução, ou **false** se for interrompido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




