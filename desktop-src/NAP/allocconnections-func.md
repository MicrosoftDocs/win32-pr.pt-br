---
title: Função AllocConnections (NapUtil. h)
description: Aloca memória para um número especificado de estruturas de conexões.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- Função AllocConnections NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645249"
---
# <a name="allocconnections-function"></a><span data-ttu-id="5e38f-104">Função AllocConnections</span><span class="sxs-lookup"><span data-stu-id="5e38f-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="5e38f-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="5e38f-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e38f-106">A função **AllocConnections** aloca memória para um número especificado de estruturas de [**conexões**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="5e38f-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e38f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e38f-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="5e38f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e38f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e38f-109">*conexões* \[ do entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5e38f-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e38f-110">Um ponteiro para uma matriz de estruturas de [**conexões**](connections-struct.md) alocadas recentemente.</span><span class="sxs-lookup"><span data-stu-id="5e38f-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="5e38f-111">*connectionsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e38f-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e38f-112">O número de estruturas para alocar a *conexões*.</span><span class="sxs-lookup"><span data-stu-id="5e38f-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e38f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e38f-113">Return value</span></span>



| <span data-ttu-id="5e38f-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5e38f-114">Return code</span></span>                                                                                   | <span data-ttu-id="5e38f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e38f-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e38f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e38f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5e38f-117">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="5e38f-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="5e38f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5e38f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5e38f-119">Um argumento inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="5e38f-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="5e38f-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5e38f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5e38f-121">O sistema está sem memória virtual.</span><span class="sxs-lookup"><span data-stu-id="5e38f-121">The system is out of virtual memory.</span></span> <span data-ttu-id="5e38f-122">Esta operação falhou.</span><span class="sxs-lookup"><span data-stu-id="5e38f-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e38f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e38f-123">Remarks</span></span>

<span data-ttu-id="5e38f-124">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="5e38f-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="5e38f-125">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="5e38f-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="5e38f-126">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5e38f-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="5e38f-127">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5e38f-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="5e38f-128">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="5e38f-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e38f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e38f-129">Requirements</span></span>



| <span data-ttu-id="5e38f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e38f-130">Requirement</span></span> | <span data-ttu-id="5e38f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5e38f-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5e38f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e38f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5e38f-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e38f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5e38f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e38f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5e38f-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e38f-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5e38f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e38f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e38f-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e38f-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="5e38f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5e38f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e38f-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e38f-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e38f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e38f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e38f-141">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="5e38f-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 





