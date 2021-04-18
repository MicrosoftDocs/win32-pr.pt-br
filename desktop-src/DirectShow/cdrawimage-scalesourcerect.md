---
description: O método ScaleSourceRect dimensiona um retângulo, se houver uma diferença entre o tamanho do vídeo nativo e o formato do tipo de mídia.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Método CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756634"
---
# <a name="cdrawimagescalesourcerect-method"></a>Método CDrawImage. ScaleSourceRect

O `ScaleSourceRect` método dimensionará um retângulo se houver uma diferença entre o tamanho do vídeo nativo e o formato do tipo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSource* 
</dt> <dd>

Ponteiro para um retângulo não dimensionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o retângulo dimensionado.

## <a name="remarks"></a>Comentários

Na classe **CDrawImage** , esse método retorna *pSource* sem nenhuma alteração. Você pode substituir esse método se o filtro alongar a imagem de vídeo de entrada. Por exemplo, o tamanho de vídeo nativo pode ser 320 240, mas o tipo de mídia no pino de entrada pode ser 640 480. Nesse caso, o filtro precisaria dimensionar o retângulo de origem por um fator de 2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




