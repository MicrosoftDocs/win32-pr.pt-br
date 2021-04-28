---
description: Método CPosPassThru. GetMediaTime – o método GetMediaTime recupera os carimbos de data/hora no exemplo atual.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Método CPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095254"
---
# <a name="cpospassthrugetmediatime-method"></a>Método CPosPassThru. GetMediaTime

O `GetMediaTime` método recupera os carimbos de data/hora no exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStartTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início, em unidades do formato de hora atual.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de término, em unidades do formato de hora atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ falha.

## <a name="remarks"></a>Comentários

Substitua esse método se o filtro armazenar em cache os carimbos de data/hora nos exemplos que receber.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




