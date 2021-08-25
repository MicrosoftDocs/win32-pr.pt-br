---
description: 'Método CPosPassThru. setpositiones – o método SetPositions define a posição atual e a posição de parada. Esse método implementa o método IMediaSeeking:: setposicionations.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Método CPosPassThru. setpositiones (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d5ed5a25c5ceb4cbe96571ef83945fdf5edd1bbd373de875f7339c13c1b43dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909186"
---
# <a name="cpospassthrusetpositions-method"></a>Método CPosPassThru. setpositiones

O `SetPositions` método define a posição atual e a posição de parada. Esse método implementa o método [**IMediaSeeking:: Setposicionations**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Ponteiro para uma variável que especifica a posição atual, em unidades do formato de hora atual.

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

Combinação bit-a-de de sinalizadores. Consulte [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obter mais informações.

</dd> <dt>

*pStop* 
</dt> <dd>

Ponteiro para uma variável que especifica a hora de parada, em unidades do formato de hora atual.

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

Combinação bit-a-de de sinalizadores. Consulte [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obter mais informações.

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

 

 




