---
description: A função GetBitmapSubtype retorna o GUID do subtipo de mídia para o bitmap especificado.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Função GetBitmapSubtype (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759297"
---
# <a name="getbitmapsubtype-function"></a>Função GetBitmapSubtype

A `GetBitmapSubtype` função retorna o **GUID** do subtipo de mídia para o bitmap especificado.

## <a name="syntax"></a>Sintaxe


```C++
const GUID GetBitmapSubtype(
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

Retorna o **GUID** do subtipo de mídia.

## <a name="remarks"></a>Comentários

Para tipos RGB não compactados, essa função mapeia o campo **biBitCount** para o subtipo. Para tipos de vídeo compactados, essa função usa a classe [**FOURCCMap**](fourccmap.md) para mapear o campo de **bicompactação** para o subtipo.

Se a função não puder corresponder ao formato de um subtipo, o valor de retorno será o GUID \_ NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de vídeo e imagem](video-and-image-functions.md)
</dt> </dl>

 

 




