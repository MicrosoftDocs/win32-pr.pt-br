---
description: O método CopyPalette copia a paleta de qualquer estrutura VIDEOINFO para qualquer estrutura palettized VIDEOINFO.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Método CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754157"
---
# <a name="cimagepalettecopypalette-method"></a>Método CImagePalette. CopyPalette

O `CopyPalette` método copia a paleta de qualquer estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) para qualquer estrutura **VIDEOINFO** palettized.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Ponteiro para o tipo de mídia de origem.

</dd> <dt>

*pDest* 
</dt> <dd>

Ponteiro para o tipo de mídia de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se a paleta tiver sido copiada. Retornará S \_ false se o tipo de mídia de origem ou de destino não tiver uma paleta.

## <a name="remarks"></a>Comentários

O tipo de mídia *pDest* deve ser um formato palettized com uma intensidade de cor de 8 bits ou menos. O tipo de mídia *pSrc* pode ser qualquer tipo de [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com uma paleta, incluindo formatos YUV e true-color com entradas de paleta. O método copia as entradas da paleta de *pSrc* em uma nova paleta e anexa a nova paleta a *pDest*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




