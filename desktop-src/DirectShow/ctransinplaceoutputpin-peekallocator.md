---
description: Método CTransInPlaceOutputPin.PeekAllocator – o método PeekAllocator retorna um ponteiro para o alocador do pino. O método não incrementa a contagem de referência na interface .
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Método CTransInPlaceOutputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b8833780411ae126dcda20c579fc5f6a681362da3707ee68879b06800b7b032
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654764"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>Método CTransInPlaceOutputPin.PeekAllocator

O `PeekAllocator` método retorna um ponteiro para o alocador do pino. O método não incrementa a contagem de referência na interface .

## <a name="syntax"></a>Sintaxe


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna a [**variável de membro CBaseOutputPin::m \_ pAllocator.**](cbaseoutputpin-m-pallocator.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




