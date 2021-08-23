---
description: Define a parte FOURCC do objeto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: Método FOURCCMap::Set LTDCC (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ac14c7174fde7184bfdbfbb5d82d3fc1288d46ff37158bbbab146c34db5ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536826"
---
# <a name="fourccmapsetfourcc-method"></a>Método FOURCCMap::SetCCICC

Define a **parte FOURCC** do [**objeto FOURCCMap.**](fourccmap.md)

## <a name="syntax"></a>Sintaxe


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pguid* 
</dt> <dd>

Ponteiro para a parte guid **(identificador** global exclusivo) retornada do **objeto FOURCCMap.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Fourcc.h (include Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




