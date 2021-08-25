---
description: O método DrawVideoImageHere desenha uma imagem de um exemplo de mídia para um contexto de dispositivo especificado.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Método CDrawImage. DrawVideoImageHere (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8137c4e18708ce6a0402d1d34caf9560054f267d8de0280a6efb5c3dd36e6517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909806"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>Método CDrawImage. DrawVideoImageHere

O `DrawVideoImageHere` método desenha uma imagem de um exemplo de mídia para um contexto de dispositivo especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* 
</dt> <dd>

Identificador para um contexto de dispositivo, onde o desenho ocorrerá.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo que contém a imagem.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Ponteiro para um retângulo de origem a ser usado para desenhar. Se for **NULL**, o retângulo em [**CDrawImage:: m \_ SourceRect**](cdrawimage-m-sourcerect.md) será usado.

</dd> <dt>

*lprcDst* 
</dt> <dd>

Ponteiro para um retângulo de destino a ser usado para desenhar. Se for **NULL**, o retângulo em [**CDrawImage:: m \_ TargetRect**](cdrawimage-m-targetrect.md) será usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




