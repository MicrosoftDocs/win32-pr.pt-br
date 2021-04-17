---
description: O método SetTargetRect define o retângulo de destino.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Método CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755352"
---
# <a name="cdrawimagesettargetrect-method"></a>Método CDrawImage. SetTargetRect

O `SetTargetRect` método define o retângulo de destino.

## <a name="syntax"></a>Sintaxe


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Ponteiro para uma estrutura **Rect** que define o novo retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro proprietário deve chamar esse método se o retângulo de origem for alterado; por exemplo, em resposta a uma chamada [**IBasicVideo:: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .

Antes de chamar esse método, valide o retângulo fornecido em *pTargetRect*, em relação à janela de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




