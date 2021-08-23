---
description: 'Interrompe o filtro. Esse método implementa o método IMediaFilter:: Stop.'
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: Método CTransformFilter. Stop (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8be126441ccbc672b54a8a9df7c296ef5f74b5a711f75617e962e5d85b11c3b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584876"
---
# <a name="ctransformfilterstop-method"></a>Método CTransformFilter. Stop

Interrompe o filtro. Esse método implementa o método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Depois que esse método desconfirma ambos os alocadores, ele chama o método [**StopStreaming**](ctransformfilter-stopstreaming.md) . O método **StopStreaming** não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




