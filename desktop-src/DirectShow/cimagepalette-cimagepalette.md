---
description: Construtor de CImagePalette. CImagePalette-método de construtor.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Construtor CImagePalette. CImagePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085674"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Construtor CImagePalette. CImagePalette

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBaseFilter* 
</dt> <dd>

Ponteiro para proprietário do filtro.

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

Ponteiro para um objeto **CBaseWindow** , que gerencia a janela onde a paleta é percebida. Este parâmetro pode ser **NULL**.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Ponteiro para um objeto **CDrawImage** , que desenha a imagem de vídeo. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




