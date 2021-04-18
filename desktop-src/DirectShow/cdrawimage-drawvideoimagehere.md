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
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752293"
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

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




