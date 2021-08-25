---
description: Método do construtor. O construtor obtém acesso ao pino especificado.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Construtor CAutoUsingOutputPin.CAutoUsingOutputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0594eed7f253f7e540f843dfc3c3de6481d7dbede3f25d1534e52181ef0585b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057516"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Construtor CAutoUsingOutputPin.CAutoUsingOutputPin

Método do construtor. O construtor obtém acesso ao pino especificado.

## <a name="syntax"></a>Sintaxe


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOutputPin* 
</dt> <dd>

Ponteiro para um [**objeto CDynamicOutputPin.**](cdynamicoutputpin.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que contém um **valor HRESULT.** O valor deve ser S \_ OK.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o método retorna, o valor *\* de phr* indica o êxito ou a falha do método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




