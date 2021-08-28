---
description: Indica se o objeto foi alterado desde que foi salvo pela última vez em seu fluxo atual.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Método CPersistStream.IsDirty (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e28285bd5660d6ba81fe77718cd9d38f325c51184a7bbd035cf3d7cb2ce6aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108436"
---
# <a name="cpersiststreamisdirty-method"></a>Método CPersistStream.IsDirty

Indica se o objeto foi alterado desde que foi salvo pela última vez em seu fluxo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o filtro precisar ser salvo e S FALSE se ele não precisar ser \_ salvo.

## <a name="remarks"></a>Comentários

Essa função membro implementa o **método IPersistStream::IsDirty.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pstream.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




