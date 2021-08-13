---
description: O método Run notifica o pino de que o filtro agora está em execução.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Método CBasePin.Run (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f145a827546a9258ee2968d0348ab7725147bb47132f5df5acbd2865a45b78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429806"
---
# <a name="cbasepinrun-method"></a>Método CBasePin.Run

O `Run` método notifica o pino de que o filtro agora está em execução.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tstart* 
</dt> <dd>

Hora de início, conforme passado para o método [**IMediaFilter::Run do**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) filtro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando o filtro passa de pausa para em execução, a [**classe CBaseFilter**](cbasefilter.md) chama esse método em todos os pinos do filtro.

Esse método não faz nada na classe base. Classes derivadas podem substituir esse método. Por exemplo, um pin pode iniciar um thread de trabalho que fornece exemplos.

O estado interno do gerenciador de grafo de filtro não é atualizado até que essa função membro retorne, portanto, não teste o estado desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




