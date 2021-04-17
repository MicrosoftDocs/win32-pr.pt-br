---
description: Recupera os estilos de um determinado atributo.
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: Função PIMEStyleFromAttr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751127"
---
# <a name="pimestylefromattr-function"></a>Função PIMEStyleFromAttr

Recupera os estilos de um determinado atributo.

## <a name="syntax"></a>Sintaxe


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*attr* \[ no\]
</dt> <dd>

Esse parâmetro pode usar um dos valores a seguir.

<dl> <dt>

<span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR \_ FIXEDCONVERTED** (5)
</dt> <dt>

<span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR \_ ENTRADA** (0)
</dt> <dt>

<span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR \_ \_Erro de entrada** (4)
</dt> <dt>

<span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR \_ MÁX** . (5)
</dt> <dt>

<span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR \_ MÍN** . (0)
</dt> <dt>

<span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR \_ DESTINO \_ convertido** (1)
</dt> <dt>

<span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR \_ DESTINO não \_ convertido** (4)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um ponteiro para uma estrutura **IMESTYLE** que representa as configurações de cor e não cor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

A estrutura **IMESTYLE** é definida da seguinte maneira:

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



 

 
