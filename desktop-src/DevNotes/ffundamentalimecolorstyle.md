---
description: Especifica se a cor especificada é uma cor fundamental.
ms.assetid: 9a06fadc-9b97-4f7d-9488-688b72d14bc5
title: Função FFundamentalIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FFundamentalIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c7de1bf4ef84d159d673e1039ad6ea328153b216
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751753"
---
# <a name="ffundamentalimecolorstyle-function"></a><span data-ttu-id="614d0-103">Função FFundamentalIMEColorStyle</span><span class="sxs-lookup"><span data-stu-id="614d0-103">FFundamentalIMEColorStyle function</span></span>

<span data-ttu-id="614d0-104">Especifica se a cor especificada é uma cor fundamental.</span><span class="sxs-lookup"><span data-stu-id="614d0-104">Specifies whether the specified color is a fundamental color.</span></span>

## <a name="syntax"></a><span data-ttu-id="614d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="614d0-105">Syntax</span></span>


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="614d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="614d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614d0-107">*pcolorstyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="614d0-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="614d0-108">Uma estrutura **IMECOLORSTY** retornada da função [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="614d0-108">An **IMECOLORSTY** structure returned from the [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614d0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="614d0-109">Return value</span></span>

<span data-ttu-id="614d0-110">Retorna **true** quando a cor é uma cor fundamental.</span><span class="sxs-lookup"><span data-stu-id="614d0-110">Returns **TRUE** when the color is a fundamental color.</span></span>

## <a name="remarks"></a><span data-ttu-id="614d0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="614d0-111">Remarks</span></span>

<span data-ttu-id="614d0-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="614d0-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="614d0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="614d0-113">Requirements</span></span>



| <span data-ttu-id="614d0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="614d0-114">Requirement</span></span> | <span data-ttu-id="614d0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="614d0-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="614d0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="614d0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="614d0-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="614d0-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="614d0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="614d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614d0-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="614d0-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="614d0-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="614d0-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
