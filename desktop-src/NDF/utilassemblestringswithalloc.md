---
title: Função UtilAssembleStringsWithAlloc (Ndattributils. h)
description: Aloca uma cadeia de caracteres e formata-a usando cadeias de caracteres fornecidas pela tabela de cadeias. Essa função usa StringCchPrintf para criar a cadeia de caracteres formatada.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- NDF da função UtilAssembleStringsWithAlloc
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645245"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="6b3e5-105">Função UtilAssembleStringsWithAlloc</span><span class="sxs-lookup"><span data-stu-id="6b3e5-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="6b3e5-106">A função **UtilAssembleStringsWithAlloc** aloca uma cadeia de caracteres e formata-a usando cadeias de caracteres fornecidas pela tabela de cadeias.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="6b3e5-107">Essa função usa [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) para criar a cadeia de caracteres formatada.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3e5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b3e5-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="6b3e5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b3e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b3e5-110">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3e5-111">Tipo: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="6b3e5-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="6b3e5-112">O local onde a cadeia de caracteres alocada recentemente será colocada.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="6b3e5-113">Quando a cadeia de caracteres não for mais necessária, ela deverá ser liberada com [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="6b3e5-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="6b3e5-114">*BufferMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3e5-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-115">Type: **UINT**</span></span>

<span data-ttu-id="6b3e5-116">O número máximo de caracteres permitidos na cadeia de caracteres alocada pelo *buffer*.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="6b3e5-117">Se a cadeia de caracteres formatada resultante for maior que o número de caracteres especificados, ela será truncada e terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="6b3e5-118">Este parâmetro não pode ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="6b3e5-119">*InputFormat* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3e5-120">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="6b3e5-121">Recurso de cadeia de caracteres fora da tabela de cadeia de caracteres que representa um parâmetro de formato passado para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span><span class="sxs-lookup"><span data-stu-id="6b3e5-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="6b3e5-122">Ele é construído usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="6b3e5-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="6b3e5-123">O formato da cadeia de caracteres do recurso deve especificar um parâmetro de formato que assume uma cadeia de caracteres larga ou um parâmetro de formato que leva uma cadeia de caracteres longa e não assinada.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="6b3e5-124">*Entradastring* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3e5-125">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="6b3e5-126">Recurso de cadeia de caracteres fora da tabela de cadeia de caracteres que representa um argumento passado para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) no lugar da cadeia de caracteres larga no parâmetro format.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="6b3e5-127">Ele é construído usando [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span><span class="sxs-lookup"><span data-stu-id="6b3e5-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="6b3e5-128">*AdditionalArgument* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3e5-129">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="6b3e5-130">True se *adicionalvalue* deve ser passado como o primeiro argumento de formatação para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); caso contrário, false (e somente a cadeia de caracteres de recurso identificada por *InputString* será passada).</span><span class="sxs-lookup"><span data-stu-id="6b3e5-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="6b3e5-131">*Adicionalvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3e5-132">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-132">Type: **ULONG**</span></span>

<span data-ttu-id="6b3e5-133">O valor a ser passado como o primeiro argumento de formatação para [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) se *AdditionalArgument* for true.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b3e5-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b3e5-134">Return value</span></span>

<span data-ttu-id="6b3e5-135">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-135">Type: **HRESULT**</span></span>

<span data-ttu-id="6b3e5-136">Os valores de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6b3e5-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6b3e5-137">Return code</span></span>                                                                                  | <span data-ttu-id="6b3e5-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b3e5-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b3e5-139"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b3e5-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6b3e5-140">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="6b3e5-141"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6b3e5-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6b3e5-142">Um ou mais parâmetros não foram fornecidos corretamente.</span><span class="sxs-lookup"><span data-stu-id="6b3e5-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6b3e5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b3e5-143">Requirements</span></span>



| <span data-ttu-id="6b3e5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b3e5-144">Requirement</span></span> | <span data-ttu-id="6b3e5-145">Valor</span><span class="sxs-lookup"><span data-stu-id="6b3e5-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b3e5-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b3e5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6b3e5-147">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6b3e5-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b3e5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6b3e5-149">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b3e5-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6b3e5-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b3e5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b3e5-151"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b3e5-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b3e5-152">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6b3e5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3e5-153">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="6b3e5-154">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="6b3e5-155">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="6b3e5-156">**MAKEINTRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="6b3e5-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="6b3e5-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

