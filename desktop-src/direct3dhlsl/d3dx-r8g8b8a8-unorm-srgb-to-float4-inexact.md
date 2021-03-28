---
title: Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Desempacota \_ \_ \_ \_ os dados do sombreador R8G8B8A8 UNORM sRGB no formato dxgi para um XMFLOAT4. | Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d3d4a9d47eb520d151fe2e3388e99f401fc0a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930640"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="cbc53-105">D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ função inexata</span><span class="sxs-lookup"><span data-stu-id="cbc53-105">D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="cbc53-106">Desempacota \_ \_ \_ \_ os dados do sombreador R8G8B8A8 UNORM sRGB no formato dxgi para um XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="cbc53-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc53-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbc53-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="cbc53-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbc53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc53-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="cbc53-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc53-110">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="cbc53-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc53-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbc53-111">Return value</span></span>

<span data-ttu-id="cbc53-112">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="cbc53-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc53-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbc53-113">Remarks</span></span>

<span data-ttu-id="cbc53-114">Essa função usa instruções de sombreador que não têm precisão alta o suficiente para fornecer a resposta exata.</span><span class="sxs-lookup"><span data-stu-id="cbc53-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="cbc53-115">A função alternativa [**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ para \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de sRGB para float.</span><span class="sxs-lookup"><span data-stu-id="cbc53-115">The alternative function [**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc53-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc53-116">Requirements</span></span>



| <span data-ttu-id="cbc53-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc53-117">Requirement</span></span> | <span data-ttu-id="cbc53-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cbc53-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc53-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbc53-119">Header</span></span><br/> | <dl> <span data-ttu-id="cbc53-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="cbc53-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc53-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbc53-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc53-122">Funções</span><span class="sxs-lookup"><span data-stu-id="cbc53-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="cbc53-123">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="cbc53-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





