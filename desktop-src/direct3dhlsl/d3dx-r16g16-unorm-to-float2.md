---
title: Função D3DX_R16G16_UNORM_to_FLOAT2
description: Desempacota \_ o formato dxgi \_ R16G16 \_ UNORM dados do sombreador para um XMFLOAT2.
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- Função D3DX_R16G16_UNORM_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba4ca1bb02e66289ec66d0ec4f58978800f6538
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298560"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a><span data-ttu-id="e3e6e-104">D3DX \_ R16G16 \_ UNORM \_ \_ FLOAT2 function</span><span class="sxs-lookup"><span data-stu-id="e3e6e-104">D3DX\_R16G16\_UNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="e3e6e-105">Desempacota \_ o formato dxgi \_ R16G16 \_ UNORM dados do sombreador para um XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="e3e6e-105">Unpacks DXGI\_FORMAT\_R16G16\_UNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e6e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3e6e-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="e3e6e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3e6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e6e-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="e3e6e-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e3e6e-109">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="e3e6e-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e6e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3e6e-110">Return value</span></span>

<span data-ttu-id="e3e6e-111">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="e3e6e-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e6e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3e6e-112">Requirements</span></span>



| <span data-ttu-id="e3e6e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e6e-113">Requirement</span></span> | <span data-ttu-id="e3e6e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e3e6e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e6e-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3e6e-115">Header</span></span><br/> | <dl> <span data-ttu-id="e3e6e-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e3e6e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e6e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3e6e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e6e-118">Funções</span><span class="sxs-lookup"><span data-stu-id="e3e6e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e3e6e-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="e3e6e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





