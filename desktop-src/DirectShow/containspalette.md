---
description: A função ContainsPalette determina se uma estrutura VIDEOINFOHEADER especificada contém uma paleta.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Função ContainsPalette (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c9e5ab793dfaadb868cc09cfbe25e59c02dc338b470992b81ab1990581e5c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954165"
---
# <a name="containspalette-function"></a>Função ContainsPalette

A **função ContainsPalette** determina se uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contém uma paleta.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Ponteiro para uma [**estrutura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se o bitdepth for 8 ou menor (**bmiHeader.biBitCount**) ou o número de índices de cores for maior que zero (**bmiHeader.biClrUsed**). Retorna **FALSE caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




