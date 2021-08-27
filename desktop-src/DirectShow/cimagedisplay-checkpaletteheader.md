---
description: O método CheckPaletteHeader valida as entradas da paleta em uma estrutura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Método CImageDisplay.CheckPaletteHeader (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6378a93ffced86546b8e95071e7f9bdc1398cdd1831aa18d41d62c6ea97caff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087286"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Método CImageDisplay.CheckPaletteHeader

O `CheckPaletteHeader` método valida as entradas da paleta em uma estrutura [**VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="syntax"></a>Sintaxe


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInput* 
</dt> <dd>

Ponteiro para uma **estrutura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** as entradas da paleta são válidas ou **FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Se o formato de imagem não for palettized, o método verificará se **biClrUsed** é igual a zero. Caso contrário, o método verificará se o **sinalizador biCompression** é BI \_ RGB; **biClr Importante** não é maior que **biClrUsed**; e o número de entradas de paleta não excede o máximo, considerando a profundidade da cor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




