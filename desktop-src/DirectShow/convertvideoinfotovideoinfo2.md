---
description: A função ConvertVideoInfoToVideoInfo2 converte um tipo de mídia que usa VIDEOINFOHEADER em um que usa VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Função ConvertVideoInfoToVideoInfo2 (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f1865652edf01a612ba7d1a46520f92a8461c9ba53a80395e27e6252e0018ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073760"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>Função ConvertVideoInfoToVideoInfo2

A `ConvertVideoInfoToVideoInfo2` função converte um tipo de mídia que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) em um que usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para a estrutura [**AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser convertida. A estrutura deve ter o tipo de formato FORMAT \_ VideoInfo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função aloca uma nova estrutura **VIDEOINFOHEADER2,** copia os membros da estrutura **VIDEOINFOHEADER** para ela e substitui a estrutura antiga pela nova estrutura no bloco de formato do tipo de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




