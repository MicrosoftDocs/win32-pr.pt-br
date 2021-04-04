---
title: Função AllocFixupInfo (NapUtil. h)
description: Aloca memória para uma estrutura FixupInfo do tamanho especificado.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- Função AllocFixupInfo NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824214"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="11f25-104">Função AllocFixupInfo</span><span class="sxs-lookup"><span data-stu-id="11f25-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="11f25-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="11f25-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="11f25-106">A função **AllocFixupInfo** aloca memória para uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) do tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="11f25-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f25-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11f25-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="11f25-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11f25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f25-109">*fixupInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="11f25-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="11f25-110">Um ponteiro para o endereço de uma estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) alocada recentemente.</span><span class="sxs-lookup"><span data-stu-id="11f25-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="11f25-111">*countResultCodes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11f25-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f25-112">O número de códigos de resultado a serem alocados ao *fixupInfo*.</span><span class="sxs-lookup"><span data-stu-id="11f25-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f25-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11f25-113">Return value</span></span>



| <span data-ttu-id="11f25-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="11f25-114">Return code</span></span>                                                                                   | <span data-ttu-id="11f25-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="11f25-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11f25-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11f25-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="11f25-117">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="11f25-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="11f25-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="11f25-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="11f25-119">Um argumento inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="11f25-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="11f25-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="11f25-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="11f25-121">O sistema está sem memória virtual.</span><span class="sxs-lookup"><span data-stu-id="11f25-121">The system is out of virtual memory.</span></span> <span data-ttu-id="11f25-122">Esta operação falhou.</span><span class="sxs-lookup"><span data-stu-id="11f25-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="11f25-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="11f25-123">Remarks</span></span>

<span data-ttu-id="11f25-124">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="11f25-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="11f25-125">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="11f25-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="11f25-126">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="11f25-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="11f25-127">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="11f25-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="11f25-128">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="11f25-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="11f25-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f25-129">Requirements</span></span>



| <span data-ttu-id="11f25-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f25-130">Requirement</span></span> | <span data-ttu-id="11f25-131">Valor</span><span class="sxs-lookup"><span data-stu-id="11f25-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="11f25-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11f25-132">Minimum supported client</span></span><br/> | <span data-ttu-id="11f25-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11f25-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="11f25-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11f25-134">Minimum supported server</span></span><br/> | <span data-ttu-id="11f25-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11f25-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="11f25-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11f25-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="11f25-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="11f25-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="11f25-138">DLL</span><span class="sxs-lookup"><span data-stu-id="11f25-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f25-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f25-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f25-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="11f25-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f25-141">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="11f25-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 





