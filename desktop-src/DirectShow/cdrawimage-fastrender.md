---
description: O método FastRender desenha a imagem de vídeo usando as funções BitBlt ou StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Método CDrawImage. FastRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754991"
---
# <a name="cdrawimagefastrender-method"></a>Método CDrawImage. FastRender

O `FastRender` método desenha a imagem de vídeo usando as funções **BitBlt** ou **StretchBlt** .

## <a name="syntax"></a>Sintaxe


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo que contém a imagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O método [**CDrawImage::D RawImage**](cdrawimage-drawimage.md) chama esse método, mas somente se o alocador da conexão for um objeto [**CImageAllocator**](cimageallocator.md) . Nesse caso, é garantido que o exemplo de mídia seja um objeto [**CImageSample**](cimagesample.md) . O objeto **CImageSample** usa a função **CreateDIBSection** para alocar memória compartilhada para o bitmap, o que torna possível desenhar a imagem usando **BitBlt** ou **StretchBlt**.

Esse método chama **BitBlt** se os retângulos de origem e destino correspondem exatamente ou **StretchBlt** de outra forma.

Se o filtro não possuir o alocador, o método **DrawImage** usará [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) para desenhar a imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




