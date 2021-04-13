---
title: Método IDWriteFontFallback MapCharacters
description: Determina uma fonte apropriada a ser usada para renderizar o intervalo inicial de texto.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Gravação direta do método MapCharacters
- Método MapCharacters Direct Write, interface IDWriteFontFallback
- IDWriteFontFallback interface de gravação direta, método MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295815"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="110ee-106">Método IDWriteFontFallback:: MapCharacters</span><span class="sxs-lookup"><span data-stu-id="110ee-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="110ee-107">Determina uma fonte apropriada a ser usada para renderizar o intervalo inicial de texto.</span><span class="sxs-lookup"><span data-stu-id="110ee-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="110ee-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="110ee-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="110ee-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="110ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="110ee-110">*source*</span><span class="sxs-lookup"><span data-stu-id="110ee-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="110ee-111">Tipo: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="110ee-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="110ee-112">A implementação da fonte de texto contém o texto e a localidade.</span><span class="sxs-lookup"><span data-stu-id="110ee-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="110ee-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="110ee-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="110ee-114">Type: **UINT32**</span></span>

<span data-ttu-id="110ee-115">Posição inicial para analisar.</span><span class="sxs-lookup"><span data-stu-id="110ee-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-116">*textLength*</span><span class="sxs-lookup"><span data-stu-id="110ee-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="110ee-117">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="110ee-117">Type: **UINT32**</span></span>

<span data-ttu-id="110ee-118">Comprimento do texto a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="110ee-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-119">*baseFontCollection* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="110ee-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="110ee-120">Tipo: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="110ee-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="110ee-121">Coleção de fontes padrão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="110ee-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-122">_baseFamilyName \* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="110ee-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="110ee-123">Tipo: \**const WCHAR \_ t \** _</span><span class="sxs-lookup"><span data-stu-id="110ee-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="110ee-124">Nome da família da fonte base.</span><span class="sxs-lookup"><span data-stu-id="110ee-124">Family name of the base font.</span></span> <span data-ttu-id="110ee-125">Se você passar NULL, nenhuma correspondência será feita em relação à família.</span><span class="sxs-lookup"><span data-stu-id="110ee-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="110ee-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="110ee-127">Tipo: **[ **\_ \_ espessura da fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="110ee-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="110ee-128">O peso desejado.</span><span class="sxs-lookup"><span data-stu-id="110ee-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-129">*basestyle*</span><span class="sxs-lookup"><span data-stu-id="110ee-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="110ee-130">Tipo: **[ **\_ \_ estilo de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="110ee-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="110ee-131">O estilo desejado.</span><span class="sxs-lookup"><span data-stu-id="110ee-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-132">*baseStretch*</span><span class="sxs-lookup"><span data-stu-id="110ee-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="110ee-133">Tipo: **[ **DWRITE \_ fonte \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="110ee-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="110ee-134">A ampliação desejada.</span><span class="sxs-lookup"><span data-stu-id="110ee-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-135">*mappedLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="110ee-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="110ee-136">Tipo: \**UINT32 \** _</span><span class="sxs-lookup"><span data-stu-id="110ee-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="110ee-137">Comprimento do texto mapeado para a fonte mapeada.</span><span class="sxs-lookup"><span data-stu-id="110ee-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="110ee-138">Isso sempre será menor ou igual ao tamanho do texto e maior que zero (se o comprimento do texto for diferente de zero), o chamador avançará pelo menos um caractere.</span><span class="sxs-lookup"><span data-stu-id="110ee-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="110ee-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="110ee-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="110ee-140">Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="110ee-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="110ee-141">A fonte que deve ser usada para renderizar os primeiros caracteres *mappedLength* do texto.</span><span class="sxs-lookup"><span data-stu-id="110ee-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="110ee-142">Se ele retornar NULL, isso significa que nenhuma fonte pode renderizar o texto e *mappedLength* é o número de caracteres a serem ignorados (renderizado com um glifo ausente).</span><span class="sxs-lookup"><span data-stu-id="110ee-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="110ee-143">*escala* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="110ee-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="110ee-144">Tipo: \**float \** _</span><span class="sxs-lookup"><span data-stu-id="110ee-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="110ee-145">Fator de escala para multiplicar o tamanho em em da fonte retornada por.</span><span class="sxs-lookup"><span data-stu-id="110ee-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="110ee-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="110ee-146">Return value</span></span>

<span data-ttu-id="110ee-147">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="110ee-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="110ee-148">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="110ee-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="110ee-149">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="110ee-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="110ee-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="110ee-150">Requirements</span></span>



| <span data-ttu-id="110ee-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="110ee-151">Requirement</span></span> | <span data-ttu-id="110ee-152">Valor</span><span class="sxs-lookup"><span data-stu-id="110ee-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="110ee-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="110ee-153">Minimum supported client</span></span><br/> | <span data-ttu-id="110ee-154">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="110ee-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="110ee-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="110ee-155">Minimum supported server</span></span><br/> | <span data-ttu-id="110ee-156">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="110ee-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="110ee-157">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="110ee-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="110ee-158">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="110ee-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="110ee-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="110ee-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="110ee-160"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="110ee-161">DLL</span><span class="sxs-lookup"><span data-stu-id="110ee-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="110ee-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="110ee-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="110ee-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="110ee-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="110ee-164">**IDWriteFontFallback**</span><span class="sxs-lookup"><span data-stu-id="110ee-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

