---
description: 'O método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
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
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750036"
---
# <a name="ctransforminputpinendflush-method"></a>Método CTransformInputPin. EndFlush

O `EndFlush` método encerra uma operação de liberação. Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                     |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O pino de saída não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) do filtro para entregar a chamada downstream. Em seguida, ele chama o método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) do PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




