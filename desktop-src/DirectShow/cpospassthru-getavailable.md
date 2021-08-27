---
description: Método CPosPassThru.GetAvailable – o método GetAvailable recupera o intervalo de vezes em que a busca é eficiente. Esse método implementa o método IMediaSeeking::GetAvailable.
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Método CPosPassThru.GetAvailable (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1db45b20264f192b2ade7d8863f9da86d5fc02159567611eff86e9cdfff1b10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084246"
---
# <a name="cpospassthrugetavailable-method"></a>Método CPosPassThru.GetAvailable

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

Ponteiro para uma variável que recebe o tempo mais antigo para uma busca eficiente.

</dd> <dt>

*pLatest* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora mais recente para busca eficiente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o **valor HRESULT** do pino conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




