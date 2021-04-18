---
description: Buscando recursos.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Membro CSourceSeeking:: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751485"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a>Membro de CSourceSeeking:: m \_ dwSeekingCaps

Buscando recursos.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a>Comentários

Por padrão, o valor é definido como a combinação bit-a-bit dos seguintes sinalizadores:

-   Estou \_ procurando \_ CanSeekForwards
-   Estou \_ procurando \_ CanSeekBackwards
-   Estou \_ procurando \_ CanSeekAbsolute
-   Estou \_ procurando \_ CanGetStopPos
-   Estou \_ procurando \_ CanGetDuration

Se o filtro oferecer suporte a um conjunto diferente de recursos, substitua esse valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




