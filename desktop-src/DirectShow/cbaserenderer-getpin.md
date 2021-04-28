---
description: Método CBaseRenderer. GetPin – o método GetPin recupera um PIN.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer. GetPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119884"
---
# <a name="cbaserenderergetpin-method"></a>Método CBaseRenderer. GetPin

O `GetPin` método recupera um PIN.

## <a name="syntax"></a>Sintaxe


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*n* 
</dt> <dd>

Número do PIN especificado. Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o ponteiro [**\_ pInputPin CBaseRenderer:: m**](cbaserenderer-m-pinputpin.md) .

## <a name="remarks"></a>Comentários

Esse método implementa o método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) , que é puro virtual na classe **CBaseFilter** . O filtro dá suporte a exatamente um PIN (o PIN de entrada). Na primeira vez que esse método é chamado, ele cria o PIN como um novo objeto [**CRendererInputPin**](crendererinputpin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




