---
title: Função UtilLoadStringWithAlloc (Ndattributils. h)
description: Aloca e carrega uma cadeia de caracteres da tabela de recursos.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- NDF da função UtilLoadStringWithAlloc
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086496"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="595c2-104">Função UtilLoadStringWithAlloc</span><span class="sxs-lookup"><span data-stu-id="595c2-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="595c2-105">A função **UtilLoadStringWithAlloc** aloca e carrega uma cadeia de caracteres da tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="595c2-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="595c2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="595c2-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="595c2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="595c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="595c2-108">*UID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="595c2-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="595c2-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="595c2-109">Type: **UINT**</span></span>

<span data-ttu-id="595c2-110">Identificador da cadeia de caracteres a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="595c2-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="595c2-111">*ppwzBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="595c2-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="595c2-112">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="595c2-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="595c2-113">O local onde a cadeia de caracteres alocada recentemente será colocada.</span><span class="sxs-lookup"><span data-stu-id="595c2-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="595c2-114">A cadeia de caracteres deve ser liberada usando [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quando não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="595c2-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="595c2-115">*cchBufferMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="595c2-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="595c2-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="595c2-116">Type: **UINT**</span></span>

<span data-ttu-id="595c2-117">O número máximo de caracteres a serem carregados da tabela de recursos.</span><span class="sxs-lookup"><span data-stu-id="595c2-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="595c2-118">Se a cadeia de caracteres do recurso for maior que o número de caracteres especificados, ela será truncada e terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="595c2-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="595c2-119">Este parâmetro não pode ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="595c2-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="595c2-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="595c2-120">Return value</span></span>

<span data-ttu-id="595c2-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="595c2-121">Type: **HRESULT**</span></span>

<span data-ttu-id="595c2-122">Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="595c2-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="595c2-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="595c2-123">Return code</span></span>                                                                                  | <span data-ttu-id="595c2-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="595c2-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="595c2-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="595c2-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="595c2-126">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="595c2-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="595c2-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="595c2-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="595c2-128">Um ou mais parâmetros não foram fornecidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="595c2-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="595c2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="595c2-129">Requirements</span></span>



| <span data-ttu-id="595c2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="595c2-130">Requirement</span></span> | <span data-ttu-id="595c2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="595c2-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="595c2-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="595c2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="595c2-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="595c2-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="595c2-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="595c2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="595c2-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="595c2-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="595c2-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="595c2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="595c2-137"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="595c2-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="595c2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="595c2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="595c2-139">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="595c2-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="595c2-140">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="595c2-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="595c2-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="595c2-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

