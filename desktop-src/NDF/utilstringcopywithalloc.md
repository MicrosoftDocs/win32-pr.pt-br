---
title: Função UtilStringCopyWithAlloc (Ndattributils. h)
description: Aloca e copia uma cadeia de caracteres de origem.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- NDF da função UtilStringCopyWithAlloc
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789750"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="30c39-104">Função UtilStringCopyWithAlloc</span><span class="sxs-lookup"><span data-stu-id="30c39-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="30c39-105">A função **UtilStringCopyWithAlloc** aloca e copia uma cadeia de caracteres de origem.</span><span class="sxs-lookup"><span data-stu-id="30c39-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c39-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30c39-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="30c39-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30c39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c39-108">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="30c39-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30c39-109">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="30c39-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="30c39-110">O local onde o ponteiro para a memória alocada é armazenado.</span><span class="sxs-lookup"><span data-stu-id="30c39-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="30c39-111">Quando não for mais necessário, ele deve ser liberado com [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="30c39-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="30c39-112">Esse buffer é sempre terminado em nulo.</span><span class="sxs-lookup"><span data-stu-id="30c39-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="30c39-113">*BufferMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30c39-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c39-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="30c39-114">Type: **UINT**</span></span>

<span data-ttu-id="30c39-115">O número máximo de caracteres a serem lidos da *origem*.</span><span class="sxs-lookup"><span data-stu-id="30c39-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="30c39-116">*Origem* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="30c39-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c39-117">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="30c39-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="30c39-118">A cadeia de caracteres a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="30c39-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c39-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30c39-119">Return value</span></span>

<span data-ttu-id="30c39-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30c39-120">Type: **HRESULT**</span></span>

<span data-ttu-id="30c39-121">Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="30c39-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="30c39-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="30c39-122">Return code</span></span>                                                                                  | <span data-ttu-id="30c39-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="30c39-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="30c39-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30c39-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="30c39-125">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="30c39-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="30c39-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30c39-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="30c39-127">Um ou mais parâmetros não foram fornecidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="30c39-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30c39-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30c39-128">Requirements</span></span>



| <span data-ttu-id="30c39-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c39-129">Requirement</span></span> | <span data-ttu-id="30c39-130">Valor</span><span class="sxs-lookup"><span data-stu-id="30c39-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c39-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30c39-131">Minimum supported client</span></span><br/> | <span data-ttu-id="30c39-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="30c39-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30c39-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30c39-133">Minimum supported server</span></span><br/> | <span data-ttu-id="30c39-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="30c39-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="30c39-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30c39-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c39-136"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c39-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c39-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="30c39-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c39-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="30c39-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="30c39-139">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="30c39-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="30c39-140">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="30c39-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

