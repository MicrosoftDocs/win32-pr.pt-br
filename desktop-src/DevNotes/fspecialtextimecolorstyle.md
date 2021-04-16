---
description: Especifica se a cor especificada é uma cor de texto especial.
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: Função FSpecialTextIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750162"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="0dc2e-103">Função FSpecialTextIMEColorStyle</span><span class="sxs-lookup"><span data-stu-id="0dc2e-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="0dc2e-104">Especifica se a cor especificada é uma cor de texto especial.</span><span class="sxs-lookup"><span data-stu-id="0dc2e-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dc2e-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="0dc2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0dc2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc2e-107">*pcolorstyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dc2e-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2e-108">Uma estrutura **IMECOLORSTY** retornada de uma função [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc2e-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc2e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0dc2e-109">Return value</span></span>

<span data-ttu-id="0dc2e-110">Retorna **true** quando a cor é uma cor de texto especial.</span><span class="sxs-lookup"><span data-stu-id="0dc2e-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc2e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dc2e-111">Remarks</span></span>

<span data-ttu-id="0dc2e-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0dc2e-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc2e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc2e-113">Requirements</span></span>



| <span data-ttu-id="0dc2e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc2e-114">Requirement</span></span> | <span data-ttu-id="0dc2e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc2e-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc2e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0dc2e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0dc2e-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2e-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dc2e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0dc2e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc2e-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="0dc2e-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="0dc2e-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="0dc2e-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
