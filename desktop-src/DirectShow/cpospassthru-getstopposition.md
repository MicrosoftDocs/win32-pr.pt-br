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
ms.openlocfilehash: 7ee704a47074db032badfa1f02ffbf2db8c7efa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778491"
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

## <a name="return-value"></a>Retornar valor

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




