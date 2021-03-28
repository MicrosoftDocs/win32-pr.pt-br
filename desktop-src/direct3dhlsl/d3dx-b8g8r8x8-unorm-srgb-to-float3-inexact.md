---
title: Função D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
description: Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8X8 UNORM sRGB no formato dxgi para um XMFLOAT3. | Função D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- Função D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ef3f0b97ee3d5e21fef7b0227304fc5b187df2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968552"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a><span data-ttu-id="1f41f-105">D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ \_ FLOAT3 \_ função inexata</span><span class="sxs-lookup"><span data-stu-id="1f41f-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3\_inexact function</span></span>

<span data-ttu-id="1f41f-106">Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8X8 UNORM sRGB no formato dxgi para um XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="1f41f-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f41f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f41f-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="1f41f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f41f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f41f-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="1f41f-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="1f41f-110">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="1f41f-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f41f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f41f-111">Return value</span></span>

<span data-ttu-id="1f41f-112">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="1f41f-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f41f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f41f-113">Remarks</span></span>

<span data-ttu-id="1f41f-114">Essa função usa instruções de sombreador que não têm precisão alta o suficiente para fornecer a resposta exata.</span><span class="sxs-lookup"><span data-stu-id="1f41f-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="1f41f-115">A função alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ para \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de sRGB para float.</span><span class="sxs-lookup"><span data-stu-id="1f41f-115">The alternative function [**D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f41f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f41f-116">Requirements</span></span>



| <span data-ttu-id="1f41f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f41f-117">Requirement</span></span> | <span data-ttu-id="1f41f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1f41f-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f41f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f41f-119">Header</span></span><br/> | <dl> <span data-ttu-id="1f41f-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="1f41f-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f41f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f41f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f41f-122">Funções</span><span class="sxs-lookup"><span data-stu-id="1f41f-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="1f41f-123">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="1f41f-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





