---
description: Construtor de CEnumPins. CEnumPins-método de construtor.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Construtor CEnumPins. CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099224"
---
# <a name="cenumpinscenumpins-constructor"></a>Construtor CEnumPins. CEnumPins

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro no qual enumerar os Pins.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Ponteiro para a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de um enumerador para clonar ou **NULL**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se *pEnumPins* for **NULL**, esse método inicializará o enumerador para o início da sequência de enumeração. Caso contrário, ele duplica o estado interno do enumerador especificado por *pEnumPins*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




