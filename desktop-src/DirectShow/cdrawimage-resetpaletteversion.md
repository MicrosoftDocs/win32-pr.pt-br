---
description: O método ResetPaletteVersion redefine a versão da paleta. Chame esse método se o PIN do filtro de propriedade for reconectado.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Método CDrawImage. ResetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d367060c86c54fb9df5bd7b0f05cea1fa3d7b7f3316dce327fca7ce9985fadfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055956"
---
# <a name="cdrawimageresetpaletteversion-method"></a>Método CDrawImage. ResetPaletteVersion

O `ResetPaletteVersion` método redefine a versão da paleta. Chame esse método se o PIN do filtro de propriedade for reconectado.

## <a name="syntax"></a>Sintaxe


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método define o valor de **m \_ PaletteVersion** como uma constante predefinida **, \_ versão da paleta**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::GetPaletteVersion**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




