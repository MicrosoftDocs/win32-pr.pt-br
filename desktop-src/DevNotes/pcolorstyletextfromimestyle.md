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
ms.openlocfilehash: 58fb2c2830f016080ac27c48b188bbd1948406a6cb7516b3279c411c87d9c155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955715"
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

## <a name="return-value"></a>Valor retornado

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

 

 
