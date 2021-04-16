---
description: A função GetBitmapSize calcula o número de bytes exigidos por um bitmap independente de dispositivo (DIB). Essa função simplesmente chama a macro DIBSize.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Função GetBitmapSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752478"
---
# <a name="getbitmapsize-function"></a>Função GetBitmapSize

A `GetBitmapSize` função calcula o número de bytes exigidos por um bitmap independente de dispositivo (DIB). Essa função simplesmente chama a macro [**dibsize**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pHeader* 
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tamanho em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




