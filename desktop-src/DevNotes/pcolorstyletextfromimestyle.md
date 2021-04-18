---
description: Recupera o estilo de cor do texto do estilo especificado.
ms.assetid: 242c37af-5b39-4b18-9c8f-4e692f41c497
title: Função PColorStyleTextFromIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleTextFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 791fdaca4a93b0a44099306b8ae14ae4d5cb11cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749507"
---
# <a name="pcolorstyletextfromimestyle-function"></a>Função PColorStyleTextFromIMEStyle

Recupera o estilo de cor do texto do estilo especificado.

## <a name="syntax"></a>Sintaxe


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pimestyle* \[ no\]
</dt> <dd>

Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Ponteiro para uma estrutura **IMECOLORSTY** que representa o estilo de cor do texto.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

A estrutura **IMECOLORSTY** é definida da seguinte maneira:

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PIMEStyleFromAttr**](pimestylefromattr.md)
</dt> </dl>

 

 
