---
description: A função GetBitmapPalette retorna a primeira entrada da paleta em uma estrutura VIDEOINFOHEADER.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: Função GetBitmapPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785346"
---
# <a name="getbitmappalette-function"></a>Função GetBitmapPalette

A `GetBitmapPalette` função retorna a primeira entrada da paleta em uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

## <a name="syntax"></a>Sintaxe


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para a primeira entrada da paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




