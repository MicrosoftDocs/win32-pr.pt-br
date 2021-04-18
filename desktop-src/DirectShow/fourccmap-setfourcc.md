---
description: Define a parte FOURCC do objeto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Método FOURCCMap:: SetFOURCC (FOURCC. h)'
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
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796272"
---
# <a name="fourccmapsetfourcc-method"></a>Método FOURCCMap:: SetFOURCC

Define a parte **FOURCC** do objeto [**FOURCCMap**](fourccmap.md) .

## <a name="syntax"></a>Sintaxe


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguid* 
</dt> <dd>

Ponteiro para a parte do identificador global exclusivo (**GUID**) retornado do objeto **FOURCCMap** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>FourCC. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




