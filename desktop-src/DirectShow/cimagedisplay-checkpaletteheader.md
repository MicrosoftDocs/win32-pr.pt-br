---
description: O método CheckPaletteHeader valida as entradas da paleta em uma estrutura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Método CImageDisplay. CheckPaletteHeader (Winutil. h)
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
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778503"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Método CImageDisplay. CheckPaletteHeader

O `CheckPaletteHeader` método valida as entradas da paleta em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

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

Ponteiro para uma estrutura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se as entradas da paleta forem válidas ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o formato de imagem não for palettized, o método verificará se **biClrUsed** é igual a zero. Caso contrário, o método verifica se o sinalizador de **bicompressão** é bi \_ RGB; **biClrImportant** não é maior que **biClrUsed**; e o número de entradas da paleta não excede o máximo, considerando a intensidade de cor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




