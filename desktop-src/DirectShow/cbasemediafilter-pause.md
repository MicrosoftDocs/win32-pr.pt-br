---
description: Pausa o objeto. Implementa o método IMediaFilter::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Método CBaseMediaFilter. PAUSE (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d7c2f68ca8753826776c804ff63e11454110d9d5287f29a61343ce4c2dcec85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079362"
---
# <a name="cbasemediafilterpause-method"></a>Método CBaseMediaFilter. Pause

Pausa o objeto. Implementa o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Na classe base, esse método define a variável de membro de [**\_ estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) para estado em \_ pausa, mas não faz mais nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




