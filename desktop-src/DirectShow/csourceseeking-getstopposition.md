---
description: 'O método GetStopPosition recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaSeeking:: GetStopPosition.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Método CSourceSeeking. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 870ddbf77d1a29a34703d4b43ee21d02b676e8fafac9ee688384246339465732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073320"
---
# <a name="csourceseekinggetstopposition-method"></a>Método CSourceSeeking. GetStopPosition

O `GetStopPosition` método recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método [**IMediaSeeking:: GetStopPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de parada, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Valor de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

A hora de parada é especificada pela variável de membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




