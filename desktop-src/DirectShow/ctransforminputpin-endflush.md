---
description: 'Método CTransformInputPin. EndFlush – o método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Método CTransformInputPin. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095054"
---
# <a name="ctransforminputpinendflush-method"></a>Método CTransformInputPin. EndFlush

O `EndFlush` método encerra uma operação de liberação. Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Sucesso.<br/>                     |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O pino de saída não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) do filtro para entregar a chamada downstream. Em seguida, ele chama o método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) do PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




