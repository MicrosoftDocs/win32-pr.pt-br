---
description: Especifica se a cor especificada é uma cor RGB.
ms.assetid: 16b48644-c2d5-4383-836a-122f44504638
title: Função FRGBIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRGBIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: df11a2ad972791eaf7049bdef5fa927aaa4119da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748926"
---
# <a name="frgbimecolorstyle-function"></a><span data-ttu-id="d94d6-103">Função FRGBIMEColorStyle</span><span class="sxs-lookup"><span data-stu-id="d94d6-103">FRGBIMEColorStyle function</span></span>

<span data-ttu-id="d94d6-104">Especifica se a cor especificada é uma cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d94d6-104">Specifies whether the specified color is an RGB color.</span></span>

## <a name="syntax"></a><span data-ttu-id="d94d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d94d6-105">Syntax</span></span>


```C++
BOOL __cdecl FRGBIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="d94d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d94d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d94d6-107">*pcolorstyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d94d6-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d94d6-108">Uma estrutura **IMECOLORSTY** retornada de uma função [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="d94d6-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d94d6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d94d6-109">Return value</span></span>

<span data-ttu-id="d94d6-110">Retorna **true** quando a cor é uma cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d94d6-110">Returns **TRUE** when the color is an RGB color.</span></span>

## <a name="remarks"></a><span data-ttu-id="d94d6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d94d6-111">Remarks</span></span>

<span data-ttu-id="d94d6-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d94d6-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d94d6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d94d6-113">Requirements</span></span>



| <span data-ttu-id="d94d6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d94d6-114">Requirement</span></span> | <span data-ttu-id="d94d6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d94d6-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d94d6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d94d6-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d94d6-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d94d6-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d94d6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d94d6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d94d6-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="d94d6-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="d94d6-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="d94d6-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
