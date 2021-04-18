---
description: 'O método GetAvailable recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método IMediaSeeking:: GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bc661d81c49798b6fe06dc569b680e5f9839e5a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758850"
---
# <a name="csourceseekinggetavailable-method"></a>Método CSourceSeeking. GetAvailable

O `GetAvailable` método recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pEarliest* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora mais antiga para busca eficiente. A variável é definida como zero.

</dd> <dt>

*mais chapas* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora mais recente para busca eficiente. A variável é definida como o valor da variável de membro [**CSourceSeeking:: m \_ rtDuration**](csourceseeking-m-rtduration.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




