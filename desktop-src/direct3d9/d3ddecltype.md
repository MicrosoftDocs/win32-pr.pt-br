---
description: Define um tipo de dados de declaração de vértice.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Enumeração D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298525"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="b91a7-103">Enumeração D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="b91a7-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="b91a7-104">Define um tipo de dados de declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="b91a7-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b91a7-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="b91a7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b91a7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b91a7-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**</span><span class="sxs-lookup"><span data-stu-id="b91a7-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-108">Float de um componente expandido para (float, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**</span><span class="sxs-lookup"><span data-stu-id="b91a7-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-110">Float de dois componentes expandido para (float, float, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**</span><span class="sxs-lookup"><span data-stu-id="b91a7-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-112">Float de três componentes expandido para (float, float, float, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="b91a7-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-114">Float de quatro componentes expandido para (float, float, float, float).</span><span class="sxs-lookup"><span data-stu-id="b91a7-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="b91a7-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-116">Os bytes de quatro componentes, empacotados e não assinados mapeados para um intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="b91a7-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="b91a7-117">Input é um [**D3DCOLOR**](d3dcolor.md) e é expandido para a ordem RGBA.</span><span class="sxs-lookup"><span data-stu-id="b91a7-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**</span><span class="sxs-lookup"><span data-stu-id="b91a7-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-119">Byte de quatro componentes, não assinado.</span><span class="sxs-lookup"><span data-stu-id="b91a7-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**</span><span class="sxs-lookup"><span data-stu-id="b91a7-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-121">Dois componentes, com assinatura reduzida expandida para (valor, valor, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**</span><span class="sxs-lookup"><span data-stu-id="b91a7-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-123">Quatro componentes, com assinatura reduzida expandida para (valor, valor, valor, valor).</span><span class="sxs-lookup"><span data-stu-id="b91a7-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**</span><span class="sxs-lookup"><span data-stu-id="b91a7-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-125">Byte de quatro componentes com cada byte normalizado dividindo com 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="b91a7-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**</span><span class="sxs-lookup"><span data-stu-id="b91a7-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-127">Normalizado, dois componentes, com sinal curto, expandido para (primeiro curto/32767.0, segundo curto/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**</span><span class="sxs-lookup"><span data-stu-id="b91a7-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-129">Normalizado, quatro componentes, assinado curto, expandido para (primeiro curto/32767.0, segundo curto/32767.0, terceiro curto/32767.0, quarto curto/32767.0).</span><span class="sxs-lookup"><span data-stu-id="b91a7-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**</span><span class="sxs-lookup"><span data-stu-id="b91a7-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-131">Normalizado, dois componentes, curto não assinado, expandido para (primeiro curto/65535.0, curto curto/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**</span><span class="sxs-lookup"><span data-stu-id="b91a7-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-133">Normalizado, quatro componentes, curto não assinado, expandido para (primeiro curto/65535.0, segundo curto/65535.0, terceiro curto/65535.0, quarto curto/65535.0).</span><span class="sxs-lookup"><span data-stu-id="b91a7-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**</span><span class="sxs-lookup"><span data-stu-id="b91a7-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-135">Formato de três componentes, não assinados, 10 10 10 expandido para (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**</span><span class="sxs-lookup"><span data-stu-id="b91a7-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-137">Três componentes, assinados, 10 10 10 Format normalizados e expandidos para (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b91a7-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-139">Dois componentes, 16 bits, ponto flutuante expandido para (valor, valor, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b91a7-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="b91a7-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-141">Quatro componentes, 16 bits, ponto flutuante expandido para (valor, valor, valor, valor).</span><span class="sxs-lookup"><span data-stu-id="b91a7-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="b91a7-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="b91a7-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="b91a7-143">O campo de tipo na declaração não é usado.</span><span class="sxs-lookup"><span data-stu-id="b91a7-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="b91a7-144">Isso foi projetado para uso com D3DDECLMETHOD \_ UV e D3DDECLMETHOD \_ LOOKUPPRESAMPLED.</span><span class="sxs-lookup"><span data-stu-id="b91a7-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b91a7-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="b91a7-145">Remarks</span></span>

<span data-ttu-id="b91a7-146">Os dados de vértice são declarados com uma matriz de estruturas [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="b91a7-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="b91a7-147">Cada elemento na matriz contém um tipo de dados de declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="b91a7-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="b91a7-148">Use a ferramenta DirectX Caps Viewer (DXCapsViewer.exe) para ver quais tipos têm suporte em seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b91a7-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="b91a7-149">Você pode obter essa ferramenta e aprender sobre ela no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="b91a7-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="b91a7-150">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="b91a7-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b91a7-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b91a7-151">Requirements</span></span>



| <span data-ttu-id="b91a7-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91a7-152">Requirement</span></span> | <span data-ttu-id="b91a7-153">Valor</span><span class="sxs-lookup"><span data-stu-id="b91a7-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b91a7-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b91a7-154">Header</span></span><br/> | <dl> <span data-ttu-id="b91a7-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b91a7-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91a7-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="b91a7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91a7-157">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="b91a7-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b91a7-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="b91a7-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
