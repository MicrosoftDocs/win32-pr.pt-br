---
description: O método IsValid determina se um tipo principal foi atribuído a esse objeto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Método CMediaType. IsValid (mtype. h)
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
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757698"
---
# <a name="cmediatypeisvalid-method"></a>Método CMediaType. IsValid

O `IsValid` método determina se um tipo principal foi atribuído a este objeto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará **true** se um tipo principal tiver sido atribuído a este objeto. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Por padrão, os objetos [**CMediaType**](cmediatype.md) são inicializados com um tipo principal de GUID \_ NULL. Chame esse método para determinar se o objeto foi inicializado corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




