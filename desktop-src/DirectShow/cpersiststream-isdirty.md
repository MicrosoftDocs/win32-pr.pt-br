---
description: Indica se o objeto foi alterado desde que foi salvo pela última vez em seu fluxo atual.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Método CPersistStream. IsDirty (pStream. h)
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
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754149"
---
# <a name="cpersiststreamisdirty-method"></a>Método CPersistStream. IsDirty

Indica se o objeto foi alterado desde que foi salvo pela última vez em seu fluxo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se o filtro precisar salvar e S \_ false se não precisar salvar.

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método **IPersistStream:: IsDirty** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PStream. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 




