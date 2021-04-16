---
title: Função AllocCountedString (NapUtil. h)
description: Aloca memória para uma cadeia de caracteres terminada em nulo e a retorna em uma estrutura de conta.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Função AllocCountedString NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757769"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="9829f-104">Função AllocCountedString</span><span class="sxs-lookup"><span data-stu-id="9829f-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="9829f-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="9829f-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9829f-106">A função **AllocCountedString** aloca memória para uma cadeia de caracteres terminada em nulo e a retorna em uma estrutura de [**conta**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="9829f-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9829f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9829f-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="9829f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9829f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9829f-109">*contado* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9829f-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9829f-110">Um ponteiro para o endereço de uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) alocada recentemente.</span><span class="sxs-lookup"><span data-stu-id="9829f-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9829f-111">*cadeia de caracteres* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9829f-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9829f-112">Um ponteiro para a cadeia de caracteres terminada em nulo que será retornado em *contadostring*.</span><span class="sxs-lookup"><span data-stu-id="9829f-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9829f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9829f-113">Return value</span></span>



| <span data-ttu-id="9829f-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9829f-114">Return code</span></span>                                                                                   | <span data-ttu-id="9829f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9829f-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9829f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9829f-117">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="9829f-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="9829f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9829f-119">Um argumento inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="9829f-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="9829f-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9829f-121">O sistema está sem memória virtual.</span><span class="sxs-lookup"><span data-stu-id="9829f-121">The system is out of virtual memory.</span></span> <span data-ttu-id="9829f-122">Esta operação falhou.</span><span class="sxs-lookup"><span data-stu-id="9829f-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9829f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9829f-123">Remarks</span></span>

<span data-ttu-id="9829f-124">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="9829f-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="9829f-125">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="9829f-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="9829f-126">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="9829f-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="9829f-127">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="9829f-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="9829f-128">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="9829f-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="9829f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9829f-129">Requirements</span></span>



| <span data-ttu-id="9829f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9829f-130">Requirement</span></span> | <span data-ttu-id="9829f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9829f-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9829f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9829f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9829f-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9829f-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9829f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9829f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9829f-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9829f-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9829f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9829f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9829f-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="9829f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9829f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9829f-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9829f-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9829f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9829f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9829f-141">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="9829f-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 





