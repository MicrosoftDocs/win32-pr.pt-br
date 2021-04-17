---
description: Converte uma estrutura IMECOLORSTY em uma estrutura COLORREF.
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: Função RGBFromIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748493"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="81a89-103">Função RGBFromIMEColorStyle</span><span class="sxs-lookup"><span data-stu-id="81a89-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="81a89-104">Converte uma estrutura **IMECOLORSTY** em uma estrutura [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="81a89-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81a89-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="81a89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a89-107">*pcolorstyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81a89-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a89-108">Uma estrutura **IMECOLORSTY** retornada de uma função [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="81a89-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a89-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81a89-109">Return value</span></span>

<span data-ttu-id="81a89-110">Retorna uma estrutura [**COLORREF**](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="81a89-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a89-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="81a89-111">Remarks</span></span>

<span data-ttu-id="81a89-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="81a89-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a89-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a89-113">Requirements</span></span>



| <span data-ttu-id="81a89-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a89-114">Requirement</span></span> | <span data-ttu-id="81a89-115">Valor</span><span class="sxs-lookup"><span data-stu-id="81a89-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81a89-116">DLL</span><span class="sxs-lookup"><span data-stu-id="81a89-116">DLL</span></span><br/> | <dl> <span data-ttu-id="81a89-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a89-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a89-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="81a89-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a89-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="81a89-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="81a89-120">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="81a89-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="81a89-121">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="81a89-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
