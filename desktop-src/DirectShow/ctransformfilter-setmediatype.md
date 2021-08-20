---
description: O método SetMediaType é chamado quando o tipo de mídia é definido em um dos pinos do filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Método CTransformFilter.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc9331a532f6748de4e03c6972fdd555e4d5e11516d946bbd131da9acab364c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584936"
---
# <a name="ctransformfiltersetmediatype-method"></a>Método CTransformFilter.SetMediaType

O método é chamado quando o tipo de mídia é definido em um dos `SetMediaType` pinos do filtro.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*direction* 
</dt> <dd>

Membro do tipo [**enumerado PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando um pino no filtro (entrada ou saída).

</dd> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os [**métodos CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) e [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) chamam esse método quando o tipo de mídia de um pino é definido. Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




