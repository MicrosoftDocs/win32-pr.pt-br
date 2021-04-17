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
# <a name="pimestylefromattr-function"></a><span data-ttu-id="eca5f-103">Função PIMEStyleFromAttr</span><span class="sxs-lookup"><span data-stu-id="eca5f-103">PIMEStyleFromAttr function</span></span>

<span data-ttu-id="eca5f-104">Recupera os estilos de um determinado atributo.</span><span class="sxs-lookup"><span data-stu-id="eca5f-104">Retrieves styles for a given attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca5f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eca5f-105">Syntax</span></span>


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a><span data-ttu-id="eca5f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eca5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eca5f-107">*attr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eca5f-107">*attr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eca5f-108">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eca5f-108">This parameter can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="eca5f-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR \_ FIXEDCONVERTED** (5)</span><span class="sxs-lookup"><span data-stu-id="eca5f-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR\_FIXEDCONVERTED** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eca5f-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR \_ ENTRADA** (0)</span><span class="sxs-lookup"><span data-stu-id="eca5f-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR\_INPUT** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eca5f-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR \_ \_Erro de entrada** (4)</span><span class="sxs-lookup"><span data-stu-id="eca5f-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR\_INPUT\_ERROR** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eca5f-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR \_ MÁX** . (5)</span><span class="sxs-lookup"><span data-stu-id="eca5f-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR\_MAX** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eca5f-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR \_ MÍN** . (0)</span><span class="sxs-lookup"><span data-stu-id="eca5f-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR\_MIN** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eca5f-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR \_ DESTINO \_ convertido** (1)</span><span class="sxs-lookup"><span data-stu-id="eca5f-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR\_TARGET\_CONVERTED** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eca5f-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR \_ DESTINO não \_ convertido** (4)</span><span class="sxs-lookup"><span data-stu-id="eca5f-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR\_TARGET\_NOTCONVERTED** (4)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eca5f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eca5f-116">Return value</span></span>

<span data-ttu-id="eca5f-117">Retorna um ponteiro para uma estrutura **IMESTYLE** que representa as configurações de cor e não cor.</span><span class="sxs-lookup"><span data-stu-id="eca5f-117">Returns a pointer to an **IMESTYLE** structure representing the color and non-color settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="eca5f-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eca5f-118">Remarks</span></span>

<span data-ttu-id="eca5f-119">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="eca5f-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="eca5f-120">A estrutura **IMESTYLE** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="eca5f-120">The **IMESTYLE** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="eca5f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eca5f-121">Requirements</span></span>



| <span data-ttu-id="eca5f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca5f-122">Requirement</span></span> | <span data-ttu-id="eca5f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eca5f-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eca5f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eca5f-124">DLL</span></span><br/> | <dl> <span data-ttu-id="eca5f-125"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eca5f-125"><dt>Imeshare.dll</dt></span></span> </dl> |



 

 
