---
description: O método StreamingThreadUsingOutputPin determina se algum thread está executando uma operação de streaming no PIN.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Método CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769221"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Método CDynamicOutputPin. StreamingThreadUsingOutputPin

O método StreamingThreadUsingOutputPin determina se algum thread está executando uma operação de streaming no PIN.

## <a name="syntax"></a>Sintaxe


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornará **true** se um thread estiver executando uma operação de streaming no PIN. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Se algum thread retornar com êxito do método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) e não tiver feito uma chamada correspondente para o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , esse método retornará **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




