---
description: Consulta se o alocador usa exemplos de mídia somente leitura.
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: Método CBaseInputPin.IsReadOnly (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45a8fc563e9377f7308ad9ea702b16f48ea9723aa13902ef29d60e2da903ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017034"
---
# <a name="cbaseinputpinisreadonly-method"></a>Método CBaseInputPin.IsReadOnly

Consulta se o alocador usa exemplos de mídia somente leitura.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna o valor da variável de membro [**CBaseInputPin::m \_ bReadOnly.**](cbaseinputpin-m-breadonly.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




