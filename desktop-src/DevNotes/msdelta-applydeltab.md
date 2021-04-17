---
description: Usa o Delta e a origem (fornecidos como buffers) para criar uma nova cópia dos dados de destino. Os dados de saída são retornados em um buffer MSDelta alocado.
title: Função ApplyDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812434"
---
# <a name="applydeltab-function"></a><span data-ttu-id="3cdf9-104">Função ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="3cdf9-104">ApplyDeltaB function</span></span>

<span data-ttu-id="3cdf9-105">Usa o Delta e a origem (fornecidos como buffers) para criar uma nova cópia dos dados de destino.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="3cdf9-106">Os dados de saída são retornados em um buffer MSDelta alocado.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="3cdf9-107">Você deve chamar [DeltaFree](msdelta-deltafree.md) para liberar o buffer de saída após a conclusão dessa função.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="3cdf9-108">Se o Delta especificado tiver sido criado usando [PatchAPI](patchapi.md)e o sinalizador [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) for definido, MSDelta chamará PatchAPI para aplicar o Delta.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdf9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cdf9-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="3cdf9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cdf9-110">Parameters</span></span>

<span data-ttu-id="3cdf9-111">*ApplyFlags*</span><span class="sxs-lookup"><span data-stu-id="3cdf9-111">*ApplyFlags*</span></span>

<span data-ttu-id="3cdf9-112">no [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) ou [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span><span class="sxs-lookup"><span data-stu-id="3cdf9-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="3cdf9-113">*Origem*</span><span class="sxs-lookup"><span data-stu-id="3cdf9-113">*Source*</span></span>

<span data-ttu-id="3cdf9-114">no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados de origem.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="3cdf9-115">*Delta*</span><span class="sxs-lookup"><span data-stu-id="3cdf9-115">*Delta*</span></span>

<span data-ttu-id="3cdf9-116">no Uma estrutura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contém um ponteiro para o buffer que contém os dados Delta.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="3cdf9-117">*lpTarget*</span><span class="sxs-lookup"><span data-stu-id="3cdf9-117">*lpTarget*</span></span>

<span data-ttu-id="3cdf9-118">fora Ponteiro para a estrutura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) onde o destino deve ser gravado.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cdf9-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cdf9-119">Return value</span></span>

<span data-ttu-id="3cdf9-120">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="3cdf9-121">Quando a função retorna **false**, você pode chamar [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o código de erro do sistema Win32 correspondente.</span><span class="sxs-lookup"><span data-stu-id="3cdf9-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cdf9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cdf9-122">Requirements</span></span>

| <span data-ttu-id="3cdf9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cdf9-123">Requirement</span></span> | <span data-ttu-id="3cdf9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3cdf9-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdf9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cdf9-125">Header</span></span> | <span data-ttu-id="3cdf9-126">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="3cdf9-126">msdelta.h</span></span> |
| <span data-ttu-id="3cdf9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3cdf9-127">DLL</span></span> | <span data-ttu-id="3cdf9-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="3cdf9-128">msdelta.dll</span></span> |
| <span data-ttu-id="3cdf9-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="3cdf9-129">Unicode</span></span> | <span data-ttu-id="3cdf9-130">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3cdf9-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="3cdf9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cdf9-131">See also</span></span>

[<span data-ttu-id="3cdf9-132">MSDelta</span><span class="sxs-lookup"><span data-stu-id="3cdf9-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="3cdf9-133">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="3cdf9-133">DeltaFree</span></span>](msdelta-deltafree.md)
