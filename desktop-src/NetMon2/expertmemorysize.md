---
description: A função ExpertMemorySize retorna a quantidade de memória alocada pela função ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Função ExpertMemorySize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826839"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="6fc87-103">Função ExpertMemorySize</span><span class="sxs-lookup"><span data-stu-id="6fc87-103">ExpertMemorySize function</span></span>

<span data-ttu-id="6fc87-104">A função **ExpertMemorySize** retorna a quantidade de memória alocada pela função [ExpertAllocMemory](expertallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc87-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc87-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fc87-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="6fc87-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fc87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc87-107">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fc87-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc87-108">Identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="6fc87-108">Unique expert identifier.</span></span> <span data-ttu-id="6fc87-109">Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc87-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6fc87-110">*pOriginalMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fc87-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc87-111">Ponteiro para o endereço de memória do especialista alocado pelo [ExpertAllocMemory](expertallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="6fc87-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc87-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fc87-112">Return value</span></span>

<span data-ttu-id="6fc87-113">A função retorna a quantidade de memória alocada em bytes.</span><span class="sxs-lookup"><span data-stu-id="6fc87-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc87-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fc87-114">Remarks</span></span>

<span data-ttu-id="6fc87-115">Para obter informações sobre o tipo de dados de **tamanho \_ T** que o **ExpertMemorySize** retorna, consulte tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="6fc87-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc87-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc87-116">Requirements</span></span>



| <span data-ttu-id="6fc87-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc87-117">Requirement</span></span> | <span data-ttu-id="6fc87-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6fc87-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc87-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc87-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc87-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fc87-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6fc87-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc87-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc87-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fc87-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6fc87-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6fc87-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc87-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc87-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6fc87-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fc87-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fc87-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fc87-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6fc87-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6fc87-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fc87-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fc87-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




