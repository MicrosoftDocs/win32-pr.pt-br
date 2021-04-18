---
description: Método de construtor.
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
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785366"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




