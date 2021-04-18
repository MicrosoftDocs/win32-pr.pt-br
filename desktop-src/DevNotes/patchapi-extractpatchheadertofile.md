---
description: Extrai as informações de cabeçalho de um Delta.
title: Função ExtractPatchHeaderToFileA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105795496"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="d16b8-103">Função ExtractPatchHeaderToFileA/W</span><span class="sxs-lookup"><span data-stu-id="d16b8-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="d16b8-104">As funções **ExtractPatchHeaderToFileA** e **ExtractPatchHeaderToFileW** extraem as informações de cabeçalho de um Delta.</span><span class="sxs-lookup"><span data-stu-id="d16b8-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="d16b8-105">O Delta é fornecido como um caminho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d16b8-105">The delta is provided as a file path.</span></span> <span data-ttu-id="d16b8-106">O cabeçalho de saída também é gravado em um caminho fornecido.</span><span class="sxs-lookup"><span data-stu-id="d16b8-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16b8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d16b8-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="d16b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d16b8-108">Parameters</span></span>

<span data-ttu-id="d16b8-109">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="d16b8-109">*PatchFileName*</span></span>

<span data-ttu-id="d16b8-110">O nome do Delta que contém o cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d16b8-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="d16b8-111">*PatchHeaderFileName*</span><span class="sxs-lookup"><span data-stu-id="d16b8-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="d16b8-112">O nome do arquivo de cabeçalho a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d16b8-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="d16b8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d16b8-113">Return value</span></span>

<span data-ttu-id="d16b8-114">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d16b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d16b8-115">Requirements</span></span>

| <span data-ttu-id="d16b8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d16b8-116">Requirement</span></span> | <span data-ttu-id="d16b8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d16b8-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d16b8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d16b8-118">Header</span></span> | <span data-ttu-id="d16b8-119">patchapi. h</span><span class="sxs-lookup"><span data-stu-id="d16b8-119">patchapi.h</span></span> |
| <span data-ttu-id="d16b8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d16b8-120">DLL</span></span> | <span data-ttu-id="d16b8-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="d16b8-121">mspatchc.dll</span></span> |
| <span data-ttu-id="d16b8-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="d16b8-122">Unicode</span></span> | <span data-ttu-id="d16b8-123">Implementado como ExtractPatchHeaderToFileW (Unicode) e ExtractPatchHeaderToFileA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d16b8-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d16b8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d16b8-124">See also</span></span>

[<span data-ttu-id="d16b8-125">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="d16b8-125">PatchAPI</span></span>](patchapi.md)
