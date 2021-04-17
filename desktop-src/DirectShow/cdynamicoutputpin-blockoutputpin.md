---
description: O método BlockOutputPin bloqueia o PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Método CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749838"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Método CDynamicOutputPin. BlockOutputPin

O `BlockOutputPin` método bloqueia o PIN. Enquanto o PIN é bloqueado, o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) aguarda que o PIN se torne desbloqueado. O estado bloqueado impede que o pino de saída entregue amostras, altere seu formato de saída ou se reconecte a si mesmo.

## <a name="syntax"></a>Sintaxe


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Antes de chamar esse método, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) . Não chame esse método se um thread de streaming estiver usando o PIN, seja para entregar dados ou para alterar a conexão. Para verificar se um thread de streaming está usando o PIN, chame o método [**CDynamicOutputPin:: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




