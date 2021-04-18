---
description: Cria um Delta entre o arquivo de origem especificado e o arquivo de destino especificado.
title: Função CreatePatchFileExA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794636"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="ae147-103">Função CreatePatchFileExA/W</span><span class="sxs-lookup"><span data-stu-id="ae147-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="ae147-104">As funções **CreatePatchFileExA** e **CreatePatchFileExW** criam um Delta entre o arquivo de origem especificado e o arquivo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="ae147-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="ae147-105">Os arquivos de origem e de destino são fornecidos como caminhos.</span><span class="sxs-lookup"><span data-stu-id="ae147-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="ae147-106">O Delta de saída também é gravado em um caminho fornecido.</span><span class="sxs-lookup"><span data-stu-id="ae147-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="ae147-107">Essas funções fornecem relatórios de andamento durante o processo de criação.</span><span class="sxs-lookup"><span data-stu-id="ae147-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae147-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae147-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="ae147-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae147-109">Parameters</span></span>

<span data-ttu-id="ae147-110">*OldFileCount*</span><span class="sxs-lookup"><span data-stu-id="ae147-110">*OldFileCount*</span></span>

<span data-ttu-id="ae147-111">O número total de arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="ae147-111">The total number of source files.</span></span> <span data-ttu-id="ae147-112">Usado para criar deltas em vários arquivos de origem (máximo de 255).</span><span class="sxs-lookup"><span data-stu-id="ae147-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="ae147-113">*OldFileInfoArray*</span><span class="sxs-lookup"><span data-stu-id="ae147-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="ae147-114">Ponteiro para a matriz de informações do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="ae147-114">Pointer to source file information array.</span></span>

<span data-ttu-id="ae147-115">*NewFilename*</span><span class="sxs-lookup"><span data-stu-id="ae147-115">*NewFileName*</span></span>

<span data-ttu-id="ae147-116">O nome do arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ae147-116">The name of the target file.</span></span>

<span data-ttu-id="ae147-117">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="ae147-117">*PatchFileName*</span></span>

<span data-ttu-id="ae147-118">O nome do Delta que é criado.</span><span class="sxs-lookup"><span data-stu-id="ae147-118">The name of the delta that is created.</span></span>

<span data-ttu-id="ae147-119">*OptionFlags*</span><span class="sxs-lookup"><span data-stu-id="ae147-119">*OptionFlags*</span></span>

<span data-ttu-id="ae147-120">Sinalizadores de criação.</span><span class="sxs-lookup"><span data-stu-id="ae147-120">Creation flags.</span></span>

<span data-ttu-id="ae147-121">*ProgressCallback*</span><span class="sxs-lookup"><span data-stu-id="ae147-121">*ProgressCallback*</span></span>

<span data-ttu-id="ae147-122">Ponteiro para retorno de chamada de progresso definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae147-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="ae147-123">*CallbackContext*</span><span class="sxs-lookup"><span data-stu-id="ae147-123">*CallbackContext*</span></span>

<span data-ttu-id="ae147-124">Ponteiro para contexto definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae147-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae147-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae147-125">Return value</span></span>

<span data-ttu-id="ae147-126">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="ae147-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae147-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae147-127">Requirements</span></span>

| <span data-ttu-id="ae147-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae147-128">Requirement</span></span> | <span data-ttu-id="ae147-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ae147-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae147-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae147-130">Header</span></span> | <span data-ttu-id="ae147-131">patchapi. h</span><span class="sxs-lookup"><span data-stu-id="ae147-131">patchapi.h</span></span> |
| <span data-ttu-id="ae147-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ae147-132">DLL</span></span> | <span data-ttu-id="ae147-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="ae147-133">mspatchc.dll</span></span> |
| <span data-ttu-id="ae147-134">Unicode</span><span class="sxs-lookup"><span data-stu-id="ae147-134">Unicode</span></span> | <span data-ttu-id="ae147-135">Implementado como CreatePatchFileExW (Unicode) e CreatePatchFileExA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ae147-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae147-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae147-136">See also</span></span>

[<span data-ttu-id="ae147-137">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="ae147-137">PatchAPI</span></span>](patchapi.md)
