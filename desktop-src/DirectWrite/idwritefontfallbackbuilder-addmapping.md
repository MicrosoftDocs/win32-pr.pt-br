---
title: Método AddMapping IDWriteFontFallbackBuilder
description: Anexa um único mapeamento à lista. Chame isso uma vez para cada mapeamento adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Método AddMapping Direct Write
- Método AddMapping Direct Write, interface IDWriteFontFallbackBuilder
- Interface IDWriteFontFallbackBuilder Direct Write, Método AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369747"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="390e4-107">Método IDWriteFontFallbackBuilder:: AddMapping</span><span class="sxs-lookup"><span data-stu-id="390e4-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="390e4-108">Anexa um único mapeamento à lista.</span><span class="sxs-lookup"><span data-stu-id="390e4-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="390e4-109">Chame isso uma vez para cada mapeamento adicional.</span><span class="sxs-lookup"><span data-stu-id="390e4-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="390e4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="390e4-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="390e4-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="390e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390e4-112">*varia*</span><span class="sxs-lookup"><span data-stu-id="390e4-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="390e4-113">Tipo: \**\* [**\_ \_ intervalo Unicode DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)* _</span><span class="sxs-lookup"><span data-stu-id="390e4-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="390e4-114">Intervalos Unicode que se aplicam a esse mapeamento.</span><span class="sxs-lookup"><span data-stu-id="390e4-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="390e4-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="390e4-116">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="390e4-116">Type: **UINT32**</span></span>

<span data-ttu-id="390e4-117">Número de intervalos Unicode.</span><span class="sxs-lookup"><span data-stu-id="390e4-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-118">*targetFamilyNames* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="390e4-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="390e4-119">Tipo: **const WCHAR \* \***</span><span class="sxs-lookup"><span data-stu-id="390e4-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="390e4-120">Lista de cadeias de caracteres de nome de família de destino.</span><span class="sxs-lookup"><span data-stu-id="390e4-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-121">*targetFamilyNamesCount*</span><span class="sxs-lookup"><span data-stu-id="390e4-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="390e4-122">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="390e4-122">Type: **UINT32**</span></span>

<span data-ttu-id="390e4-123">Número de nomes de família de destino.</span><span class="sxs-lookup"><span data-stu-id="390e4-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-124">*fonte de fontes* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="390e4-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="390e4-125">Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="390e4-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="390e4-126">Coleção de fontes explícita opcional para este mapeamento.</span><span class="sxs-lookup"><span data-stu-id="390e4-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-127">*localename* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="390e4-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="390e4-128">Tipo: \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="390e4-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="390e4-129">Localidade do contexto.</span><span class="sxs-lookup"><span data-stu-id="390e4-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-130">_baseFamilyName \* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="390e4-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="390e4-131">Tipo: \**const WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="390e4-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="390e4-132">Nome da família base com a qual corresponder, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="390e4-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="390e4-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="390e4-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="390e4-134">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="390e4-134">Type: **FLOAT**</span></span>

<span data-ttu-id="390e4-135">Fator de escala para multiplicar a fonte de destino do resultado por.</span><span class="sxs-lookup"><span data-stu-id="390e4-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390e4-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="390e4-136">Return value</span></span>

<span data-ttu-id="390e4-137">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="390e4-137">Type: **HRESULT**</span></span>

<span data-ttu-id="390e4-138">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="390e4-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="390e4-139">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="390e4-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="390e4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="390e4-140">Requirements</span></span>



| <span data-ttu-id="390e4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="390e4-141">Requirement</span></span> | <span data-ttu-id="390e4-142">Valor</span><span class="sxs-lookup"><span data-stu-id="390e4-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="390e4-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="390e4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="390e4-144">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="390e4-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="390e4-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="390e4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="390e4-146">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="390e4-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="390e4-147">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="390e4-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="390e4-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="390e4-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="390e4-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="390e4-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="390e4-150"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="390e4-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="390e4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="390e4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="390e4-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="390e4-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="390e4-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="390e4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390e4-154">**IDWriteFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="390e4-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

