---
title: Função D3DX_B8G8R8X8_UNORM_to_FLOAT3
description: Desempacota \_ o formato dxgi \_ B8G8R8X8 \_ UNORM dados do sombreador para um XMFLOAT3.
ms.assetid: 0987d71a-89a4-4751-9f32-08e2490204d2
keywords:
- Função D3DX_B8G8R8X8_UNORM_to_FLOAT3 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6397f271899c2a8d73ed1ba84a04f3c02514fb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968551"
---
# <a name="d3dx_b8g8r8x8_unorm_to_float3-function"></a><span data-ttu-id="1c506-104">D3DX \_ B8G8R8X8 \_ UNORM \_ \_ FLOAT3 function</span><span class="sxs-lookup"><span data-stu-id="1c506-104">D3DX\_B8G8R8X8\_UNORM\_to\_FLOAT3 function</span></span>

<span data-ttu-id="1c506-105">Desempacota \_ o formato dxgi \_ B8G8R8X8 \_ UNORM dados do sombreador para um XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="1c506-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c506-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c506-106">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="1c506-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c506-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c506-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="1c506-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="1c506-109">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="1c506-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c506-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c506-110">Return value</span></span>

<span data-ttu-id="1c506-111">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="1c506-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c506-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c506-112">Requirements</span></span>



| <span data-ttu-id="1c506-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c506-113">Requirement</span></span> | <span data-ttu-id="1c506-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1c506-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c506-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c506-115">Header</span></span><br/> | <dl> <span data-ttu-id="1c506-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="1c506-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c506-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c506-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c506-118">Funções</span><span class="sxs-lookup"><span data-stu-id="1c506-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="1c506-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="1c506-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





