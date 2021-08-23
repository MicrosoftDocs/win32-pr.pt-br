---
description: Construtor CImagePalette.CImagePalette – Método do construtor.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Construtor CImagePalette.CImagePalette (Winutil.h)
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
ms.openlocfilehash: 437055ee9e1d33d4b551faf1ca999d432a99d17919dcd67f6a701bc4f9780543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428916"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Construtor CImagePalette.CImagePalette

Método do construtor.

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

Ponteiro para filtro de propriedade.

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

Ponteiro para um **objeto CBaseWindow,** que gerencia a janela em que a paleta é realizada. Este parâmetro pode ser **NULL**.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Ponteiro para um **objeto CDrawImage,** que desenha a imagem de vídeo. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




