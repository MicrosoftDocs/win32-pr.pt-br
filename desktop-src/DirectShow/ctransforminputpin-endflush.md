---
description: Método CTransformInputPin.EndFlush – o método EndFlush encerra uma operação de liberação. Esse método implementa o método IPin::EndFlush.
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Método CTransformInputPin.EndFlush (Transfrm.h)
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
ms.openlocfilehash: bca2231f36c3d37f58bb740ddf55132d1c63babba6054629b2a76cc5d7866646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687216"
---
# <a name="ctransforminputpinendflush-method"></a>Método CTransformInputPin.EndFlush

O `EndFlush` método encerra uma operação de liberação. Esse método implementa o [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O pino de saída não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) do filtro para entregar a chamada downstream. Em seguida, ele chama o [**método CBaseInputPin::EndFlush do**](cbaseinputpin-endflush.md) pino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




