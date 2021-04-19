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
# <a name="format-conversion-functions-hlsl-reference"></a>Funções de conversão de formato (referência HLSL)

A seção contém as funções de conversão de formato usadas em sombreadores de computação e pixel.

-   [Funções de conversor](#converter-functions)
-   [Tópicos relacionados](#related-topics)

> O cabeçalho D3DX_DXGIFormatConvert. inl é fornecido no SDK do DirectX herdado e confia no suporte a XNAMath para C++. Ele também está incluído no pacote NuGet [Microsoft. DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) . A versão mais recente usa o suporte a DirectXMath para C++ e todas as funções são definidas no namespace **DirectX** C++.

## <a name="converter-functions"></a>Funções de conversor

### <a name="dxgi_format_r10g10b10a2_unorm"></a>\_Formato dxgi \_ R10G10B10A2 \_ UNORM

<dl>

[**D3DX \_ R10G10B10A2 \_ UNORM \_ \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ \_ R10G10B10A2 \_ UNORM**](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a>\_Formato dxgi \_ R10G10B10A2 \_ uint

<dl>

[**D3DX \_ R10G10B10A2 \_ uint \_ to \_ UINT4**](d3dx-r10g10b10a2-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ \_ R10G10B10A2 \_ uint**](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a>\_UNORM do formato dxgi \_ R8G8B8A8 \_ :

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ \_ FLOAT4**](d3dx-r8g8b8a8-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM**](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a>\_Formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB

<dl>

[**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ inexato**](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM \_ sRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a>\_Formato dxgi \_ R8G8B8A8 \_ uint

<dl>

[**D3DX \_ R8G8B8A8 \_ uint \_ to \_ UINT4**](d3dx-r8g8b8a8-uint-to-uint4.md)  
[**D3DX \_ UINT4 \_ \_ R8G8B8A8 \_ uint**](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a>\_Formato dxgi \_ R8G8B8A8 \_ SNORM

<dl>

[**D3DX \_ R8G8B8A8 \_ SNORM \_ \_ FLOAT4**](d3dx-r8g8b8a8-snorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ SNORM**](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a>\_Formato dxgi \_ R8G8B8A8 \_ Santo

<dl>

[**D3DX \_ R8G8B8A8 \_ Santo \_ a \_ INT4**](d3dx-r8g8b8a8-sint-to-int4.md)  
[**D3DX \_ INT4 \_ \_ R8G8B8A8 \_ Santo**](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a>\_Formato dxgi \_ B8G8R8A8 \_ UNORM

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ \_ FLOAT4**](d3dx-b8g8r8a8-unorm-to-float4.md)  
[**D3DX \_ FLOAT4 \_ \_ B8G8R8A8 \_ UNORM**](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a>\_Formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB

<dl>

[**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ inexato**](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4**](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[**D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM \_ sRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a>\_Formato dxgi \_ B8G8R8X8 \_ UNORM

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ \_ FLOAT3**](d3dx-b8g8r8x8-unorm-to-float3.md)  
[**D3DX \_ FLOAT3 \_ \_ B8G8R8X8 \_ UNORM**](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a>\_Formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB

<dl>

[**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ \_ FLOAT3 \_ inexato**](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[**D3DX \_ FLOAT3 \_ \_ B8G8R8X8 \_ UNORM \_ sRGB**](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a>\_ \_ Float R16G16 de formato dxgi \_

<dl>

[**D3DX \_ R16G16 \_ float \_ to \_ FLOAT2**](d3dx-r16g16-float-to-float2.md)  
[**D3DX \_ FLOAT2 \_ \_ R16G16 \_ float**](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a>\_Formato dxgi \_ R16G16 \_ UNORM

<dl>

[**D3DX \_ R16G16 \_ UNORM \_ \_ FLOAT2**](d3dx-r16g16-unorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ \_ R16G16 \_ UNORM**](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a>\_Formato dxgi \_ R16G16 \_ uint

<dl>

[**D3DX \_ R16G16 \_ uint \_ to \_ UINT2**](d3dx-r16g16-uint-to-uint2.md)  
[**D3DX \_ UINT2 \_ \_ R16G16 \_ uint**](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a>\_Formato dxgi \_ R16G16 \_ SNORM

<dl>

[**D3DX \_ R16G16 \_ SNORM \_ \_ FLOAT2**](d3dx-r16g16-snorm-to-float2.md)  
[**D3DX \_ FLOAT2 \_ \_ R16G16 \_ SNORM**](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a>\_Formato dxgi \_ R16G16 \_ Santo

<dl>

[**D3DX \_ R16G16 \_ Santo \_ a \_ Int2**](d3dx-r16g16-sint-to-int2.md)  
[**D3DX \_ Int2 \_ \_ R16G16 \_ Santo**](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de conversão de formato embutido](inline-format-conversion-reference.md)
</dt> <dt>

[Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
