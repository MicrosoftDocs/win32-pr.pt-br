---
description: O método SetSourceRect define o retângulo de origem.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Método CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756602"
---
# <a name="cdrawimagesetsourcerect-method"></a>Método CDrawImage. SetSourceRect

O `SetSourceRect` método define o retângulo de origem.

## <a name="syntax"></a>Sintaxe


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Ponteiro para uma estrutura **Rect** que define o novo retângulo de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro proprietário deve chamar esse método se o retângulo de origem for alterado; por exemplo, em resposta a uma chamada [**IBasicVideo:: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .

Valide o retângulo fornecido em *pSourceRect* antes de chamar esse método, para certificar-se de que ele não ultrapasse o tamanho do vídeo nativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




