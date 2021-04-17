---
description: O método CRendererInputPin é um método de construtor.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Construtor CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757021"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>Construtor CRendererInputPin. CRendererInputPin

O `CRendererInputPin` método é um método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRenderer* 
</dt> <dd>

Ponteiro para o objeto [**CBaseRenderer**](cbaserenderer.md) que implementa o filtro.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor **HRESULT** .

</dd> <dt>

*Nome* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres largos contendo o identificador de PIN.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




