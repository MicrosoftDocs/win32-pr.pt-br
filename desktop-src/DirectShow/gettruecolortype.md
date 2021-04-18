---
description: A função GetTrueColorType recupera o nome legível por humanos de um subtipo de vídeo.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Função GetTrueColorType (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751875"
---
# <a name="gettruecolortype-function"></a>Função GetTrueColorType

A função **GetTrueColorType** recupera o nome legível por humanos de um subtipo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pHeader* 
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define o bitmap.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




