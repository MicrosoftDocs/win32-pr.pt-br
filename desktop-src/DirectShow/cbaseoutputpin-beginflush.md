---
description: 'O método BeginFlush inicia uma operação de liberação. Implementa o método IPin:: BeginFlush.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Método CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd12216fb040601d73eb566d47ec5c8c3ceeec685bd8f7abc6877756f94c6a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640006"
---
# <a name="cbaseoutputpinbeginflush-method"></a>Método CBaseOutputPin. BeginFlush

O `BeginFlush` método inicia uma operação de liberação. Implementa o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna E \_ inesperado.

## <a name="remarks"></a>Comentários

Esse método só deve ser chamado em Pins de entrada, portanto a implementação de **CBaseOutputPin** retorna E \_ inesperada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




