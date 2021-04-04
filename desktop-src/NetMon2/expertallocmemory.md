---
description: A função ExpertAllocMemory aloca memória para o especialista.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Função ExpertAllocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646801"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="f9153-103">Função ExpertAllocMemory</span><span class="sxs-lookup"><span data-stu-id="f9153-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="f9153-104">A função **ExpertAllocMemory** aloca memória para o especialista.</span><span class="sxs-lookup"><span data-stu-id="f9153-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9153-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9153-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="f9153-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9153-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="f9153-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="f9153-108">Identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f9153-108">Unique expert identifier.</span></span> <span data-ttu-id="f9153-109">Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="f9153-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f9153-110">*nbytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f9153-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9153-111">Memória alocada, medida em bytes.</span><span class="sxs-lookup"><span data-stu-id="f9153-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9153-112">*perror* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9153-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9153-113">Indicador de erro.</span><span class="sxs-lookup"><span data-stu-id="f9153-113">Error indicator.</span></span> <span data-ttu-id="f9153-114">Se a função falhar, o parâmetro *nbytes* conterá o código de erro.</span><span class="sxs-lookup"><span data-stu-id="f9153-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="f9153-115">Se o código de erro for NMERR \_ expert \_ Finalize, o especialista deverá limpar e retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f9153-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9153-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9153-116">Return value</span></span>

<span data-ttu-id="f9153-117">Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="f9153-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="f9153-118">Se a função não for bem-sucedida, o valor de retorno será **nulo** e *perror* fornecerá um código de erro que indica o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="f9153-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9153-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9153-119">Remarks</span></span>

<span data-ttu-id="f9153-120">É importante observar que um especialista deve usar as funções de alocação de memória Monitor de Rede (incluindo [ExpertReallocMemory](expertreallocmemory.md)) para o gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="f9153-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="f9153-121">Se o seu especialista falhar durante o tempo de execução, usar essas funções permitirá Monitor de Rede liberar a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="f9153-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9153-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9153-122">Requirements</span></span>



| <span data-ttu-id="f9153-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9153-123">Requirement</span></span> | <span data-ttu-id="f9153-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f9153-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9153-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9153-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f9153-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9153-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f9153-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9153-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f9153-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f9153-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f9153-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f9153-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9153-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9153-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f9153-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9153-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9153-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9153-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9153-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f9153-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9153-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9153-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




