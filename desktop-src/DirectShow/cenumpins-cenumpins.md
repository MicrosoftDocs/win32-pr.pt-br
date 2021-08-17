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
ms.openlocfilehash: 1972533b86215e34563b9b1aa8f1b8ac3c14450b804fdae01ed7c7eafa78def4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131236"
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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




