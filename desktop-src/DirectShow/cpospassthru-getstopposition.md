---
description: 'O método GetStopPosition recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaSeeking:: GetStopPosition.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Método CPosPassThru. GetStopPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9c6798d03e2935c991e12cded4d85a4972d54e7800d6aa79c70525b10276f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084066"
---
# <a name="cpospassthrugetstopposition-method"></a>Método CPosPassThru. GetStopPosition

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

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




