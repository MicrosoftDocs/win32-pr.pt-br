---
description: O método DrawImage desenha um quadro de vídeo na janela de vídeo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Método CDrawImage. DrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750051"
---
# <a name="cdrawimagedrawimage-method"></a>Método CDrawImage. DrawImage

O `DrawImage` método desenha um quadro de vídeo na janela de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL DrawImage(
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

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Esse método delega para [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) ou [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md), dependendo se o filtro possui o alocador que forneceu o exemplo. Se o filtro possuir o alocador, será garantido que o exemplo seja um objeto [**CImageSample**](cimagesample.md) . Nesse caso, o exemplo usa a memória compartilhada alocada pela GDI e a imagem pode ser desenhada usando **BitBlt** ou **StretchBlt**. Caso contrário, as imagens devem ser desenhadas usando as funções **SetDIBitsToDevice** ou **StretchDIBits** mais lentas.

Em compilações de depuração, esse método chama **DisplaySampleTimes** para desenhar os carimbos de data/hora da amostra na imagem de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




