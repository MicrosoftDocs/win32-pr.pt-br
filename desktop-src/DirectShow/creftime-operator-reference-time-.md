---
description: O operador REFERENCE \_ TIME() lança o objeto em um tipo de dados \_ REFERENCE TIME.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Método CRefTime.operator REFERENCE_TIME (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a084d4e142f57b724343ac5a353461b41aac0be216b8e3851bc8b7e40000a1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108026"
---
# <a name="creftimeoperator-reference_time-method"></a>Método CRefTime.operator REFERENCE \_ TIME

O `REFERENCE_TIME()` operador lança o objeto em um tipo de dados REFERENCE [**\_ TIME.**](reference-time.md)

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor de [**CRefTime::m \_ time**](creftime-m-time.md).

## <a name="remarks"></a>Comentários

O exemplo a seguir mostra como usar esse operador de cast:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Reftime.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




