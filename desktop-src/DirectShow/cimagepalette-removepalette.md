---
description: O método RemovePalette exclui a paleta lógica existente e chama CBaseWindow::UnsetPalette no objeto CBaseWindow.
ms.assetid: fab531b8-8630-43f8-bf08-cd8f24659bef
title: Método CImagePalette.RemovePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.RemovePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b87c8f028da17e6af305900f203c5cf1143132806ca1b2ce9b0edaddebd0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916005"
---
# <a name="cimagepaletteremovepalette-method"></a>Método CImagePalette.RemovePalette

O método exclui a paleta lógica existente e `RemovePalette` chama [**CBaseWindow::UnsetPalette**](cbasewindow-unsetpalette.md) no **objeto CBaseWindow.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemovePalette();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




