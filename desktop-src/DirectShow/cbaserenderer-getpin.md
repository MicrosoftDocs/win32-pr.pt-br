---
description: Método CBaseRenderer.GetPin – o método GetPin recupera um pin.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer.GetPin (Renbase.h)
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
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822697"
---
# <a name="cbaserenderergetpin-method"></a>Método CBaseRenderer.GetPin

O `GetPin` método recupera um pin.

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

Número do pino especificado. Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o [**ponteiro CBaseRenderer::m \_ pInputPin.**](cbaserenderer-m-pinputpin.md)

## <a name="remarks"></a>Comentários

Esse método implementa o [**método CBaseFilter::GetPin,**](cbasefilter-getpin.md) que é virtual puro na **classe CBaseFilter.** O filtro dá suporte a exatamente um pino (o pino de entrada). Na primeira vez que esse método é chamado, ele cria o pin como um novo [**objeto CRendererInputPin.**](crendererinputpin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




