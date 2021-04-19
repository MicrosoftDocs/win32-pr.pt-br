---
title: Funções de conversão de formato (referência HLSL)
description: A seção contém as funções de conversão de formato usadas em sombreadores de computação e pixel.
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 355fb59aa6a94e144daf05942b40d3f685daff51
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222874"
---
# <a name="format-conversion-functions-hlsl-reference"></a><span data-ttu-id="e86bb-103">Funções de conversão de formato (referência HLSL)</span><span class="sxs-lookup"><span data-stu-id="e86bb-103">Format conversion functions (HLSL reference)</span></span>

<span data-ttu-id="e86bb-104">A seção contém as funções de conversão de formato usadas em sombreadores de computação e pixel.</span><span class="sxs-lookup"><span data-stu-id="e86bb-104">The section contains the format conversion functions used in Compute and Pixel Shaders.</span></span>

-   [<span data-ttu-id="e86bb-105">Funções de conversor</span><span class="sxs-lookup"><span data-stu-id="e86bb-105">Converter Functions</span></span>](#converter-functions)
-   [<span data-ttu-id="e86bb-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e86bb-106">Related topics</span></span>](#related-topics)

> <span data-ttu-id="e86bb-107">O cabeçalho D3DX_DXGIFormatConvert. inl é fornecido no SDK do DirectX herdado e confia no suporte a XNAMath para C++.</span><span class="sxs-lookup"><span data-stu-id="e86bb-107">The D3DX_DXGIFormatConvert.inl header ships in the legacy DirectX SDK and relied on XNAMath for C++ support.</span></span> <span data-ttu-id="e86bb-108">Ele também está incluído no pacote NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) .</span><span class="sxs-lookup"><span data-stu-id="e86bb-108">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span> <span data-ttu-id="e86bb-109">A versão mais recente usa o suporte a DirectXMath para C++ e todas as funções são definidas no namespace **DirectX** C++.</span><span class="sxs-lookup"><span data-stu-id="e86bb-109">The latest version uses DirectXMath for C++ support, and all functions are defined in the **DirectX** C++ namespace.</span></span>

## <a name="converter-functions"></a><span data-ttu-id="e86bb-110">Funções de conversor</span><span class="sxs-lookup"><span data-stu-id="e86bb-110">Converter Functions</span></span>

### <a name="dxgi_format_r10g10b10a2_unorm"></a><span data-ttu-id="e86bb-111">\_Formato dxgi \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e86bb-111">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>

<dl>

[<span data-ttu-id="e86bb-112">**D3DX \_ R10G10B10A2 \_ UNORM \_ \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-112">**D3DX\_R10G10B10A2\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r10g10b10a2-unorm-to-float4.md)  
[<span data-ttu-id="e86bb-113">**D3DX \_ FLOAT4 \_ \_ R10G10B10A2 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-113">**D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM**</span></span>](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a><span data-ttu-id="e86bb-114">\_Formato dxgi \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e86bb-114">DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>

<dl>

[<span data-ttu-id="e86bb-115">**D3DX \_ R10G10B10A2 \_ uint \_ to \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-115">**D3DX\_R10G10B10A2\_UINT\_to\_UINT4**</span></span>](d3dx-r10g10b10a2-uint-to-uint4.md)  
[<span data-ttu-id="e86bb-116">**D3DX \_ UINT4 \_ \_ R10G10B10A2 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="e86bb-116">**D3DX\_UINT4\_to\_R10G10B10A2\_UINT**</span></span>](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a><span data-ttu-id="e86bb-117">\_UNORM do formato dxgi \_ R8G8B8A8 \_ :</span><span class="sxs-lookup"><span data-stu-id="e86bb-117">DXGI\_FORMAT\_R8G8B8A8\_UNORM:</span></span>

<dl>

[<span data-ttu-id="e86bb-118">**D3DX \_ R8G8B8A8 \_ UNORM \_ \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-118">**D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-to-float4.md)  
[<span data-ttu-id="e86bb-119">**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-119">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM**</span></span>](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a><span data-ttu-id="e86bb-120">\_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="e86bb-120">DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="e86bb-121">**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ inexato**</span><span class="sxs-lookup"><span data-stu-id="e86bb-121">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="e86bb-122">**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-122">**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="e86bb-123">**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="e86bb-123">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a><span data-ttu-id="e86bb-124">\_Formato dxgi \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e86bb-124">DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>

<dl>

[<span data-ttu-id="e86bb-125">**D3DX \_ R8G8B8A8 \_ uint \_ to \_ UINT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-125">**D3DX\_R8G8B8A8\_UINT\_to\_UINT4**</span></span>](d3dx-r8g8b8a8-uint-to-uint4.md)  
[<span data-ttu-id="e86bb-126">**D3DX \_ UINT4 \_ \_ R8G8B8A8 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="e86bb-126">**D3DX\_UINT4\_to\_R8G8B8A8\_UINT**</span></span>](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a><span data-ttu-id="e86bb-127">\_Formato dxgi \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e86bb-127">DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>

<dl>

[<span data-ttu-id="e86bb-128">**D3DX \_ R8G8B8A8 \_ SNORM \_ \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-128">**D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4**</span></span>](d3dx-r8g8b8a8-snorm-to-float4.md)  
[<span data-ttu-id="e86bb-129">**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-129">**D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM**</span></span>](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a><span data-ttu-id="e86bb-130">\_Formato dxgi \_ R8G8B8A8 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="e86bb-130">DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>

<dl>

[<span data-ttu-id="e86bb-131">**D3DX \_ R8G8B8A8 \_ Santo \_ a \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-131">**D3DX\_R8G8B8A8\_SINT\_to\_INT4**</span></span>](d3dx-r8g8b8a8-sint-to-int4.md)  
[<span data-ttu-id="e86bb-132">**D3DX \_ INT4 \_ \_ R8G8B8A8 \_ Santo**</span><span class="sxs-lookup"><span data-stu-id="e86bb-132">**D3DX\_INT4\_to\_R8G8B8A8\_SINT**</span></span>](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a><span data-ttu-id="e86bb-133">\_Formato dxgi \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e86bb-133">DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>

<dl>

[<span data-ttu-id="e86bb-134">**D3DX \_ B8G8R8A8 \_ UNORM \_ \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-134">**D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-to-float4.md)  
[<span data-ttu-id="e86bb-135">**D3DX \_ FLOAT4 \_ \_ B8G8R8A8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-135">**D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM**</span></span>](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a><span data-ttu-id="e86bb-136">\_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="e86bb-136">DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="e86bb-137">**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ inexato**</span><span class="sxs-lookup"><span data-stu-id="e86bb-137">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[<span data-ttu-id="e86bb-138">**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="e86bb-138">**D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4**</span></span>](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[<span data-ttu-id="e86bb-139">**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="e86bb-139">**D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB**</span></span>](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a><span data-ttu-id="e86bb-140">\_Formato dxgi \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e86bb-140">DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>

<dl>

[<span data-ttu-id="e86bb-141">**D3DX \_ B8G8R8X8 \_ UNORM \_ \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="e86bb-141">**D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-to-float3.md)  
[<span data-ttu-id="e86bb-142">**D3DX \_ FLOAT3 \_ \_ B8G8R8X8 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-142">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM**</span></span>](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a><span data-ttu-id="e86bb-143">\_Formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="e86bb-143">DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>

<dl>

[<span data-ttu-id="e86bb-144">**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ \_ FLOAT3 \_ inexato**</span><span class="sxs-lookup"><span data-stu-id="e86bb-144">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[<span data-ttu-id="e86bb-145">**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="e86bb-145">**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**</span></span>](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[<span data-ttu-id="e86bb-146">**D3DX \_ FLOAT3 \_ \_ B8G8R8X8 \_ UNORM \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="e86bb-146">**D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB**</span></span>](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a><span data-ttu-id="e86bb-147">\_ \_ Float R16G16 de formato dxgi \_</span><span class="sxs-lookup"><span data-stu-id="e86bb-147">DXGI\_FORMAT\_R16G16\_FLOAT</span></span>

<dl>

[<span data-ttu-id="e86bb-148">**D3DX \_ R16G16 \_ float \_ to \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="e86bb-148">**D3DX\_R16G16\_FLOAT\_to\_FLOAT2**</span></span>](d3dx-r16g16-float-to-float2.md)  
[<span data-ttu-id="e86bb-149">**D3DX \_ FLOAT2 \_ \_ R16G16 \_ float**</span><span class="sxs-lookup"><span data-stu-id="e86bb-149">**D3DX\_FLOAT2\_to\_R16G16\_FLOAT**</span></span>](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a><span data-ttu-id="e86bb-150">\_Formato dxgi \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="e86bb-150">DXGI\_FORMAT\_R16G16\_UNORM</span></span>

<dl>

[<span data-ttu-id="e86bb-151">**D3DX \_ R16G16 \_ UNORM \_ \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="e86bb-151">**D3DX\_R16G16\_UNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-unorm-to-float2.md)  
[<span data-ttu-id="e86bb-152">**D3DX \_ FLOAT2 \_ \_ R16G16 \_ UNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-152">**D3DX\_FLOAT2\_to\_R16G16\_UNORM**</span></span>](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a><span data-ttu-id="e86bb-153">\_Formato dxgi \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="e86bb-153">DXGI\_FORMAT\_R16G16\_UINT</span></span>

<dl>

[<span data-ttu-id="e86bb-154">**D3DX \_ R16G16 \_ uint \_ to \_ UINT2**</span><span class="sxs-lookup"><span data-stu-id="e86bb-154">**D3DX\_R16G16\_UINT\_to\_UINT2**</span></span>](d3dx-r16g16-uint-to-uint2.md)  
[<span data-ttu-id="e86bb-155">**D3DX \_ UINT2 \_ \_ R16G16 \_ uint**</span><span class="sxs-lookup"><span data-stu-id="e86bb-155">**D3DX\_UINT2\_to\_R16G16\_UINT**</span></span>](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a><span data-ttu-id="e86bb-156">\_Formato dxgi \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="e86bb-156">DXGI\_FORMAT\_R16G16\_SNORM</span></span>

<dl>

[<span data-ttu-id="e86bb-157">**D3DX \_ R16G16 \_ SNORM \_ \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="e86bb-157">**D3DX\_R16G16\_SNORM\_to\_FLOAT2**</span></span>](d3dx-r16g16-snorm-to-float2.md)  
[<span data-ttu-id="e86bb-158">**D3DX \_ FLOAT2 \_ \_ R16G16 \_ SNORM**</span><span class="sxs-lookup"><span data-stu-id="e86bb-158">**D3DX\_FLOAT2\_to\_R16G16\_SNORM**</span></span>](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a><span data-ttu-id="e86bb-159">\_Formato dxgi \_ R16G16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="e86bb-159">DXGI\_FORMAT\_R16G16\_SINT</span></span>

<dl>

[<span data-ttu-id="e86bb-160">**D3DX \_ R16G16 \_ Santo \_ a \_ Int2**</span><span class="sxs-lookup"><span data-stu-id="e86bb-160">**D3DX\_R16G16\_SINT\_to\_INT2**</span></span>](d3dx-r16g16-sint-to-int2.md)  
[<span data-ttu-id="e86bb-161">**D3DX \_ Int2 \_ \_ R16G16 \_ Santo**</span><span class="sxs-lookup"><span data-stu-id="e86bb-161">**D3DX\_INT2\_to\_R16G16\_SINT**</span></span>](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="e86bb-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e86bb-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e86bb-163">Referência de conversão de formato embutido</span><span class="sxs-lookup"><span data-stu-id="e86bb-163">Inline Format Conversion Reference</span></span>](inline-format-conversion-reference.md)
</dt> <dt>

[<span data-ttu-id="e86bb-164">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="e86bb-164">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
