---
description: A função ExpertFreeMemory libera a memória adquirida por chamadas para as funções ExpertAllocMemory e ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Função ExpertFreeMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757106"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="c102c-103">Função ExpertFreeMemory</span><span class="sxs-lookup"><span data-stu-id="c102c-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="c102c-104">A função **ExpertFreeMemory** libera a memória adquirida por chamadas para as funções [**ExpertAllocMemory**](expertallocmemory.md) e [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="c102c-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c102c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c102c-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="c102c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c102c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c102c-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="c102c-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="c102c-108">Identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c102c-108">Unique expert identifier.</span></span> <span data-ttu-id="c102c-109">Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="c102c-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c102c-110">*pMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c102c-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c102c-111">Ponteiro para a memória que Monitor de Rede aloca.</span><span class="sxs-lookup"><span data-stu-id="c102c-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="c102c-112">O ponteiro *pMemory* pode ser retornado por uma chamada anterior para [**ExpertAllocMemory**](expertallocmemory.md) ou [**ExpertReallocMemory**](expertreallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c102c-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c102c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c102c-113">Return value</span></span>

<span data-ttu-id="c102c-114">Se a função for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c102c-114">If the function is successful.</span></span> <span data-ttu-id="c102c-115">o valor de retorno é NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c102c-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c102c-116">Se a função não for bem-sucedida, o valor de retorno indicará o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="c102c-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="c102c-117">Se o valor de retorno for NMERR \_ expert \_ Finalize, o especialista limpará e retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c102c-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="c102c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c102c-118">Remarks</span></span>

<span data-ttu-id="c102c-119">É importante observar que um especialista deve usar as funções de alocação de memória Monitor de Rede para gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="c102c-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="c102c-120">Se o seu especialista falhar durante o tempo de execução, usar essas funções permitirá Monitor de Rede liberar a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="c102c-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="c102c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c102c-121">Requirements</span></span>



| <span data-ttu-id="c102c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c102c-122">Requirement</span></span> | <span data-ttu-id="c102c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c102c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c102c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c102c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c102c-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c102c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c102c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c102c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c102c-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c102c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c102c-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c102c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c102c-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c102c-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c102c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c102c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c102c-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c102c-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c102c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c102c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c102c-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c102c-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




