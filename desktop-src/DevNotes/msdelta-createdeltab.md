---
description: Cria um Delta entre a origem e o destino (fornecidos como buffers) e retorna o Delta de saída como um buffer MSDelta.
title: Função CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772766"
---
# <a name="createdeltab-function"></a><span data-ttu-id="2e91b-103">Função CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="2e91b-103">CreateDeltaB function</span></span>

<span data-ttu-id="2e91b-104">Cria um Delta entre a origem e o destino (fornecidos como buffers) e retorna o Delta de saída como um buffer MSDelta.</span><span class="sxs-lookup"><span data-stu-id="2e91b-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="2e91b-105">Você deve chamar [DeltaFree](msdelta-deltafree.md) para liberar o buffer de saída após a conclusão dessa função.</span><span class="sxs-lookup"><span data-stu-id="2e91b-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e91b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e91b-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="2e91b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e91b-107">Parameters</span></span>

<span data-ttu-id="2e91b-108">*Filetypeset*</span><span class="sxs-lookup"><span data-stu-id="2e91b-108">*FileTypeSet*</span></span>

<span data-ttu-id="2e91b-109">no O valor [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) que indica o conjunto de tipos de arquivo a ser usado para o processo de criação.</span><span class="sxs-lookup"><span data-stu-id="2e91b-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="2e91b-110">*SetFlags*</span><span class="sxs-lookup"><span data-stu-id="2e91b-110">*SetFlags*</span></span>

<span data-ttu-id="2e91b-111">no Um ou mais valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especificam os sinalizadores a serem usados durante o processo de criação, além dos sinalizadores padrão.</span><span class="sxs-lookup"><span data-stu-id="2e91b-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="2e91b-112">*ResetFlags*</span><span class="sxs-lookup"><span data-stu-id="2e91b-112">*ResetFlags*</span></span>

<span data-ttu-id="2e91b-113">no Um ou mais valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especificam os sinalizadores padrão a serem redefinidos durante o processo de criação.</span><span class="sxs-lookup"><span data-stu-id="2e91b-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="2e91b-114">*Origem*</span><span class="sxs-lookup"><span data-stu-id="2e91b-114">*Source*</span></span>

<span data-ttu-id="2e91b-115">no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de origem.</span><span class="sxs-lookup"><span data-stu-id="2e91b-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="2e91b-116">*Target (destino)*</span><span class="sxs-lookup"><span data-stu-id="2e91b-116">*Target*</span></span>

<span data-ttu-id="2e91b-117">no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de destino.</span><span class="sxs-lookup"><span data-stu-id="2e91b-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="2e91b-118">*Origemoptions*</span><span class="sxs-lookup"><span data-stu-id="2e91b-118">*SourceOptions*</span></span>

<span data-ttu-id="2e91b-119">[in] Reservado.</span><span class="sxs-lookup"><span data-stu-id="2e91b-119">[in] Reserved.</span></span> <span data-ttu-id="2e91b-120">Passe uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) com *editável* definido como **false**, *lpStart* definido como **nulo** e *uSize* definido como 0.</span><span class="sxs-lookup"><span data-stu-id="2e91b-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="2e91b-121">*Targetoptions*</span><span class="sxs-lookup"><span data-stu-id="2e91b-121">*TargetOptions*</span></span>

<span data-ttu-id="2e91b-122">[in] Reservado.</span><span class="sxs-lookup"><span data-stu-id="2e91b-122">[in] Reserved.</span></span> <span data-ttu-id="2e91b-123">Passe uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) com *editável* definido como **false**, *lpStart* definido como **nulo** e *uSize* definido como 0.</span><span class="sxs-lookup"><span data-stu-id="2e91b-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="2e91b-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="2e91b-124">*GlobalOptions*</span></span>

<span data-ttu-id="2e91b-125">[in] Reservado.</span><span class="sxs-lookup"><span data-stu-id="2e91b-125">[in] Reserved.</span></span> <span data-ttu-id="2e91b-126">Passe uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) com *LpStart* definido como **nulo** e *uSize* definido como 0.</span><span class="sxs-lookup"><span data-stu-id="2e91b-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="2e91b-127">*lpTargetFileTime*</span><span class="sxs-lookup"><span data-stu-id="2e91b-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="2e91b-128">no O carimbo de data/hora definido no arquivo de destino após a aplicação Delta.</span><span class="sxs-lookup"><span data-stu-id="2e91b-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="2e91b-129">Se for **NULL**, o carimbo de data/hora de destino será a hora atual durante o processo de criação.</span><span class="sxs-lookup"><span data-stu-id="2e91b-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="2e91b-130">*HashAlgId*</span><span class="sxs-lookup"><span data-stu-id="2e91b-130">*HashAlgId*</span></span>

<span data-ttu-id="2e91b-131">no ALG_ID do algoritmo a ser usado para gerar a assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2e91b-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="2e91b-132">Alguns valores especiais são:</span><span class="sxs-lookup"><span data-stu-id="2e91b-132">Some special values are:</span></span>

- <span data-ttu-id="2e91b-133">0 = sem assinatura</span><span class="sxs-lookup"><span data-stu-id="2e91b-133">0 = No signature</span></span>
- <span data-ttu-id="2e91b-134">32 = CRC de 32 bits definida em msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="2e91b-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="2e91b-135">*lpDelta*</span><span class="sxs-lookup"><span data-stu-id="2e91b-135">*lpDelta*</span></span>

<span data-ttu-id="2e91b-136">fora Ponteiro para a estrutura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) onde o Delta deve ser gravado.</span><span class="sxs-lookup"><span data-stu-id="2e91b-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e91b-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e91b-137">Return value</span></span>

<span data-ttu-id="2e91b-138">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="2e91b-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="2e91b-139">Quando a função retorna **false**, você pode chamar [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o código de erro do sistema Win32 correspondente.</span><span class="sxs-lookup"><span data-stu-id="2e91b-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e91b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e91b-140">Requirements</span></span>

| <span data-ttu-id="2e91b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e91b-141">Requirement</span></span> | <span data-ttu-id="2e91b-142">Valor</span><span class="sxs-lookup"><span data-stu-id="2e91b-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e91b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e91b-143">Header</span></span> | <span data-ttu-id="2e91b-144">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="2e91b-144">msdelta.h</span></span> |
| <span data-ttu-id="2e91b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2e91b-145">DLL</span></span> | <span data-ttu-id="2e91b-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="2e91b-146">msdelta.dll</span></span> |
| <span data-ttu-id="2e91b-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="2e91b-147">Unicode</span></span> | <span data-ttu-id="2e91b-148">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="2e91b-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="2e91b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e91b-149">See also</span></span>

[<span data-ttu-id="2e91b-150">MSDelta</span><span class="sxs-lookup"><span data-stu-id="2e91b-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="2e91b-151">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="2e91b-151">DeltaFree</span></span>](msdelta-deltafree.md)
