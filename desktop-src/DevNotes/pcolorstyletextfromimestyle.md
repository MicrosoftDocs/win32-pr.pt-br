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
# <a name="pcolorstyletextfromimestyle-function"></a><span data-ttu-id="87e13-103">Função PColorStyleTextFromIMEStyle</span><span class="sxs-lookup"><span data-stu-id="87e13-103">PColorStyleTextFromIMEStyle function</span></span>

<span data-ttu-id="87e13-104">Recupera o estilo de cor do texto do estilo especificado.</span><span class="sxs-lookup"><span data-stu-id="87e13-104">Retrieves the text color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e13-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87e13-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleTextFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="87e13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e13-107">*pimestyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87e13-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e13-108">Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="87e13-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e13-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87e13-109">Return value</span></span>

<span data-ttu-id="87e13-110">Ponteiro para uma estrutura **IMECOLORSTY** que representa o estilo de cor do texto.</span><span class="sxs-lookup"><span data-stu-id="87e13-110">Pointer to an **IMECOLORSTY** structure representing the text color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e13-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="87e13-111">Remarks</span></span>

<span data-ttu-id="87e13-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="87e13-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="87e13-113">A estrutura **IMECOLORSTY** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="87e13-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="87e13-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87e13-114">Requirements</span></span>



| <span data-ttu-id="87e13-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="87e13-115">Requirement</span></span> | <span data-ttu-id="87e13-116">Valor</span><span class="sxs-lookup"><span data-stu-id="87e13-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87e13-117">DLL</span><span class="sxs-lookup"><span data-stu-id="87e13-117">DLL</span></span><br/> | <dl> <span data-ttu-id="87e13-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87e13-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e13-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="87e13-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e13-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="87e13-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
