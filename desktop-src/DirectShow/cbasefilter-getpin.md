---
description: O método GetPin recupera um PIN. A classe CEnumPins chama esse método para enumerar Pins no filtro.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Método CBaseFilter. GetPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755392"
---
# <a name="cbasefiltergetpin-method"></a>Método CBaseFilter. GetPin

O método **GetPin** recupera um PIN. A classe [**CEnumPins**](cenumpins.md) chama esse método para enumerar Pins no filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

O índice de base zero do PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN.

## <a name="remarks"></a>Comentários

Você deve implementar esse método virtual puro em sua classe derivada. Retornar um ponteiro para o *n* º PIN neste filtro, indexado de zero. Você pode escolher uma ordem de indexação arbitrária, desde que a ordem seja fixa. Se o filtro Adicionar ou excluir Pins ou a ordenação for alterada por algum outro motivo em tempo de execução, chame o método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




