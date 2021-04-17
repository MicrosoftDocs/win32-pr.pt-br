---
description: O método GetReader retorna um ponteiro para a interface IAsyncReader do pino de saída.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Método CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754976"
---
# <a name="cpullpingetreader-method"></a>Método CPullPin. GetReader

O `GetReader` método retorna um ponteiro para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) do pino de saída.

## <a name="syntax"></a>Sintaxe


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

## <a name="remarks"></a>Comentários

A interface retornada tem uma contagem de referência pendente. O chamador deve liberar a interface.

O método não verifica o valor do ponteiro de interface antes de chamar **AddRef**, portanto, não chame isso até que você tenha chamado o método [**CPullPin:: Connect**](cpullpin-connect.md) com êxito. Caso contrário, o ponteiro de interface pode ser **nulo** e chamar **AddRef** gerará uma exceção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




