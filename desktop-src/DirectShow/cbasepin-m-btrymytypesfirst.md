---
description: Sinalizador que indica se o pino tenta seus próprios tipos de mídia preferenciais antes daqueles do pino de recebimento.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: Membro CBasePin::m_bTryMyTypesFirst (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df94a95783d15c09fd53bd8659db71f2ce0b1aefe5d855fef5f5a03e71445493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158367"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Membro CBasePin::m \_ bTryMyTypesFirst

Sinalizador que indica se o pino tenta seus próprios tipos de mídia preferenciais antes daqueles do pino de recebimento.

## <a name="syntax"></a>Sintaxe


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Comentários

Esse sinalizador assume FALSE como **padrão.** Se o sinalizador for **TRUE,** o [**método CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) reverterá a ordem na qual ele tenta tipos de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




