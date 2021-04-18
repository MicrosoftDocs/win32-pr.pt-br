---
description: Recupera o estilo de cor do plano de fundo do estilo especificado.
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: Função PColorStyleBackFromIMEStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751036"
---
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="36055-103">Função PColorStyleBackFromIMEStyle</span><span class="sxs-lookup"><span data-stu-id="36055-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="36055-104">Recupera o estilo de cor do plano de fundo do estilo especificado.</span><span class="sxs-lookup"><span data-stu-id="36055-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="36055-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36055-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="36055-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36055-107">*pimestyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36055-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36055-108">Uma estrutura **IMESTYLE** retornada da função [**PIMEStyleFromAttr**](pimestylefromattr.md) .</span><span class="sxs-lookup"><span data-stu-id="36055-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36055-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36055-109">Return value</span></span>

<span data-ttu-id="36055-110">Ponteiro para uma estrutura **IMECOLORSTY** que representa o estilo de cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="36055-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="36055-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="36055-111">Remarks</span></span>

<span data-ttu-id="36055-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="36055-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="36055-113">A estrutura **IMECOLORSTY** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="36055-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="36055-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36055-114">Requirements</span></span>



| <span data-ttu-id="36055-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="36055-115">Requirement</span></span> | <span data-ttu-id="36055-116">Valor</span><span class="sxs-lookup"><span data-stu-id="36055-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36055-117">DLL</span><span class="sxs-lookup"><span data-stu-id="36055-117">DLL</span></span><br/> | <dl> <span data-ttu-id="36055-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36055-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36055-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="36055-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36055-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="36055-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
