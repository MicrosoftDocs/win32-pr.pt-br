---
description: O método PeekAllocator retorna um ponteiro para o alocador do PIN. O método não incrementa a contagem de referência na interface.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Método CTransInPlaceInputPin. PeekAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812787"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a>Método CTransInPlaceInputPin. PeekAllocator

O `PeekAllocator` método retorna um ponteiro para o alocador do PIN. O método não incrementa a contagem de referência na interface.

## <a name="syntax"></a>Sintaxe


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna a variável de membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




