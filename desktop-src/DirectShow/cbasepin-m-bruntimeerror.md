---
description: Sinalizador que indica se ocorreu um erro em tempo de executar.
ms.assetid: 917bcb21-a11e-4ac5-af96-565f61c155cd
title: Membro CBasePin::m_bRunTimeError (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bRunTimeError
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffc07a15f7c34744be52c5e2c7b5233e1885b58c5b9b7d078871277f8fc0efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823328"
---
# <a name="cbasepinm_bruntimeerror-member"></a>Membro CBasePin::m \_ bRunTimeError

Sinalizador que indica se ocorreu um erro em tempo de executar.

## <a name="syntax"></a>Sintaxe


```C++
bool m_bRunTimeError;
```



## <a name="remarks"></a>Comentários

Esse sinalizador assume FALSE como **padrão.** De definir o sinalizador **como TRUE** se ocorrer um erro em tempo de run time durante o streaming. O [**método CBasePin::Inactive**](cbasepin-inactive.md) redefine o sinalizador para **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




