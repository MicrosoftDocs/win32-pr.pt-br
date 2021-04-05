---
title: Método gratuito IMemoryAllocator
description: O método gratuito libera a memória alocada pelo método Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Armazenamento estruturado de método gratuito
- Armazenamento estruturado de método gratuito, interface IMemoryAllocator
- Armazenamento estruturado da interface IMemoryAllocator, método gratuito
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008966"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="2174d-106">Método IMemoryAllocator:: Free</span><span class="sxs-lookup"><span data-stu-id="2174d-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="2174d-107">O método **gratuito** libera a memória alocada pelo método [**ALLOCATE**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="2174d-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2174d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2174d-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="2174d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2174d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2174d-110">*PV*</span><span class="sxs-lookup"><span data-stu-id="2174d-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="2174d-111">Ponteiro para a memória a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="2174d-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2174d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2174d-112">Requirements</span></span>



| <span data-ttu-id="2174d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2174d-113">Requirement</span></span> | <span data-ttu-id="2174d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2174d-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2174d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2174d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2174d-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2174d-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2174d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2174d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2174d-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2174d-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2174d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2174d-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="2174d-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2174d-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





