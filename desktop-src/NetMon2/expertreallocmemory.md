---
description: A função ExpertReallocMemory aumenta ou diminui a quantidade de memória alocada por Monitor de Rede.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Função ExpertReallocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752234"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="b10b9-103">Função ExpertReallocMemory</span><span class="sxs-lookup"><span data-stu-id="b10b9-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="b10b9-104">A função **ExpertReallocMemory** aumenta ou diminui a quantidade de memória alocada por monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="b10b9-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b10b9-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="b10b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b10b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b10b9-107">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b10b9-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b10b9-108">Identificador exclusivo passado para o especialista em [**executar**](run.md) ou [**Configurar**](configure.md).</span><span class="sxs-lookup"><span data-stu-id="b10b9-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="b10b9-109">*pOriginalMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b10b9-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b10b9-110">Ponteiro para a memória alocada por Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="b10b9-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="b10b9-111">O ponteiro *pOriginalMemory* pode ser retornado por uma chamada anterior para [**ExpertAllocMemory**](expertallocmemory.md) ou **ExpertReallocMemory**.</span><span class="sxs-lookup"><span data-stu-id="b10b9-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="b10b9-112">*nbytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b10b9-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b10b9-113">Tamanho da memória realocada.</span><span class="sxs-lookup"><span data-stu-id="b10b9-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="b10b9-114">*perror* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b10b9-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b10b9-115">No retorno, um código de erro se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="b10b9-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="b10b9-116">Se o código de erro for NMERR \_ expert \_ Finalize, o especialista deverá limpar e retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b10b9-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b10b9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b10b9-117">Return value</span></span>

<span data-ttu-id="b10b9-118">Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="b10b9-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="b10b9-119">Se a função não for bem-sucedida, o valor de retorno será **nulo** e *perror* (se for um valor não **nulo** ) indica o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="b10b9-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b10b9-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b10b9-120">Remarks</span></span>

<span data-ttu-id="b10b9-121">É importante observar que um especialista deve usar as funções de alocação de memória Monitor de Rede para gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="b10b9-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="b10b9-122">Se o seu especialista falhar durante o tempo de execução, usar essas funções permitirá Monitor de Rede liberar a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="b10b9-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="b10b9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b10b9-123">Requirements</span></span>



| <span data-ttu-id="b10b9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b10b9-124">Requirement</span></span> | <span data-ttu-id="b10b9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b10b9-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b10b9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b10b9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b10b9-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b10b9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b10b9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b10b9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b10b9-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b10b9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b10b9-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b10b9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b10b9-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b10b9-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b10b9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b10b9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b10b9-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b10b9-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b10b9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b10b9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b10b9-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b10b9-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




