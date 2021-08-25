---
description: O método CopyPalette copia a paleta de qualquer estrutura VIDEOINFO para qualquer estrutura VIDEOINFO palettizada.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Método CImagePalette.CopyPalette (Winutil.h)
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
ms.openlocfilehash: 5c6f645d134ccf5fa786ff59cf0bc6cd37211af0cb2571bbc9955e5bb6367a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055446"
---
# <a name="cimagepalettecopypalette-method"></a>Método CImagePalette.CopyPalette

O `CopyPalette` método copia a paleta de qualquer estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) para qualquer estrutura **VIDEOINFO palettizada.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Psrc* 
</dt> <dd>

Ponteiro para o tipo de mídia de origem.

</dd> <dt>

*pDest* 
</dt> <dd>

Ponteiro para o tipo de mídia de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se a paleta tiver sido copiada. Retornará S FALSE se o tipo de mídia de origem ou \_ de destino não tiver uma paleta.

## <a name="remarks"></a>Comentários

O *tipo de mídia pDest* deve ser um formato palettizado com uma profundidade de cor de 8 bits ou menos. O *tipo de mídia pSrc* pode ser qualquer tipo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com uma paleta, incluindo formatos YUV e de cor verdadeira com entradas de paleta. O método copia as entradas da paleta do *pSrc* em uma nova paleta e anexa a nova paleta ao *pDest*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




