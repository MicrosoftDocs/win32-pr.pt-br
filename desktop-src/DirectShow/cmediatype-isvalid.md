---
description: O método IsValid determina se um tipo principal foi atribuído a esse objeto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Método CMediaType.IsValid (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611d36cfe19623840f102b820b2b312138b1e116d32fc399927da57e7f47300
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016254"
---
# <a name="cmediatypeisvalid-method"></a>Método CMediaType.IsValid

O `IsValid` método determina se um tipo principal foi atribuído a esse objeto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se um tipo principal tiver sido atribuído a esse objeto. Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Por padrão, [**os objetos CMediaType**](cmediatype.md) são inicializados com um tipo principal de GUID \_ NULL. Chame esse método para determinar se o objeto foi inicializado corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




