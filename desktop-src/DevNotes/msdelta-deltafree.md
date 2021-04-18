---
description: Libera o bloco de memória especificado.
title: Função DeltaFree
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105795508"
---
# <a name="deltafree-function"></a><span data-ttu-id="d2748-103">Função DeltaFree</span><span class="sxs-lookup"><span data-stu-id="d2748-103">DeltaFree function</span></span>

<span data-ttu-id="d2748-104">Libera o bloco de memória especificado.</span><span class="sxs-lookup"><span data-stu-id="d2748-104">Frees the specified memory block.</span></span> <span data-ttu-id="d2748-105">Você deve chamar essa função após chamadas bem-sucedidas para [CreateDeltaB](msdelta-createdeltab.md) e [ApplyDeltaB](msdelta-applydeltab.md) para liberar o buffer de memória alocado MSDelta.</span><span class="sxs-lookup"><span data-stu-id="d2748-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2748-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2748-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="d2748-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2748-107">Parameters</span></span>

<span data-ttu-id="d2748-108">*lpMemory*</span><span class="sxs-lookup"><span data-stu-id="d2748-108">*lpMemory*</span></span>

<span data-ttu-id="d2748-109">no Bloco de memória a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="d2748-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2748-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2748-110">Return value</span></span>

<span data-ttu-id="d2748-111">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d2748-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="d2748-112">Quando a função retorna **false**, você pode chamar [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o código de erro do sistema Win32 correspondente.</span><span class="sxs-lookup"><span data-stu-id="d2748-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2748-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2748-113">Requirements</span></span>

| <span data-ttu-id="d2748-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2748-114">Requirement</span></span> | <span data-ttu-id="d2748-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2748-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2748-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2748-116">Header</span></span> | <span data-ttu-id="d2748-117">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="d2748-117">msdelta.h</span></span> |
| <span data-ttu-id="d2748-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d2748-118">DLL</span></span> | <span data-ttu-id="d2748-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="d2748-119">msdelta.dll</span></span> |
| <span data-ttu-id="d2748-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2748-120">Unicode</span></span> | <span data-ttu-id="d2748-121">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d2748-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="d2748-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2748-122">See also</span></span>

[<span data-ttu-id="d2748-123">MSDelta</span><span class="sxs-lookup"><span data-stu-id="d2748-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="d2748-124">CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="d2748-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="d2748-125">ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="d2748-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
