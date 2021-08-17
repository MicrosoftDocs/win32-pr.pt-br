---
description: Método CSourceSeeking.GetAvailable – o método GetAvailable recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método IMediaSeeking::GetAvailable.
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking.GetAvailable (Ctlutil.h)
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
ms.openlocfilehash: ae42efad42bf9f1e0df0f4f791f1e4e8abb76fe8252818a8e35eda4dd6e6b87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953745"
---
# <a name="csourceseekinggetavailable-method"></a>Método CSourceSeeking.GetAvailable

O `GetAvailable` método recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o [**método IMediaSeeking::GetAvailable.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pEarearear* 
</dt> <dd>

Ponteiro para uma variável que recebe o tempo mais antigo para uma busca eficiente. A variável é definida como zero.

</dd> <dt>

*pLatest* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora mais recente para busca eficiente. A variável é definida como o valor da variável de membro [**CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




