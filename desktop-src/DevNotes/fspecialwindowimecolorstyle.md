---
description: Especifica se a cor especificada é uma cor de janela especial.
ms.assetid: 41f7d4fb-9718-42a8-89df-c29bd8c0665b
title: Função FSpecialWindowIMEColorStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialWindowIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 6fb667186789361a106a23f8daa82088b9bcb2ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747486"
---
# <a name="fspecialwindowimecolorstyle-function"></a><span data-ttu-id="a20ed-103">Função FSpecialWindowIMEColorStyle</span><span class="sxs-lookup"><span data-stu-id="a20ed-103">FSpecialWindowIMEColorStyle function</span></span>

<span data-ttu-id="a20ed-104">Especifica se a cor especificada é uma cor de janela especial.</span><span class="sxs-lookup"><span data-stu-id="a20ed-104">Specifies whether the specified color is a special window color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a20ed-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialWindowIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="a20ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a20ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a20ed-107">*pcolorstyle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a20ed-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a20ed-108">Uma estrutura **IMECOLORSTY** retornada de uma função [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) ou [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="a20ed-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a20ed-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a20ed-109">Return value</span></span>

<span data-ttu-id="a20ed-110">Retorna **true** quando a cor é uma cor de janela especial (uma cor especial).</span><span class="sxs-lookup"><span data-stu-id="a20ed-110">Returns **TRUE** when the color is a special window color (one of special color).</span></span>

## <a name="remarks"></a><span data-ttu-id="a20ed-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a20ed-111">Remarks</span></span>

<span data-ttu-id="a20ed-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a20ed-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20ed-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a20ed-113">Requirements</span></span>



| <span data-ttu-id="a20ed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a20ed-114">Requirement</span></span> | <span data-ttu-id="a20ed-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a20ed-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a20ed-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a20ed-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a20ed-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a20ed-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20ed-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a20ed-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20ed-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="a20ed-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="a20ed-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="a20ed-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
