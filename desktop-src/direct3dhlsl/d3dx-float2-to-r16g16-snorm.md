---
title: Função D3DX_FLOAT2_to_R16G16_SNORM
description: Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ SNORM.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- Função D3DX_FLOAT2_to_R16G16_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930628"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a><span data-ttu-id="6fe62-104">D3DX \_ FLOAT2 \_ \_ R16G16 \_ SNORM function</span><span class="sxs-lookup"><span data-stu-id="6fe62-104">D3DX\_FLOAT2\_to\_R16G16\_SNORM function</span></span>

<span data-ttu-id="6fe62-105">Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ SNORM.</span><span class="sxs-lookup"><span data-stu-id="6fe62-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe62-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fe62-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="6fe62-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fe62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe62-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="6fe62-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe62-109">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="6fe62-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe62-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fe62-110">Return value</span></span>

<span data-ttu-id="6fe62-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="6fe62-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe62-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fe62-112">Requirements</span></span>



| <span data-ttu-id="6fe62-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe62-113">Requirement</span></span> | <span data-ttu-id="6fe62-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6fe62-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe62-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fe62-115">Header</span></span><br/> | <dl> <span data-ttu-id="6fe62-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="6fe62-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe62-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fe62-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe62-118">Funções</span><span class="sxs-lookup"><span data-stu-id="6fe62-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="6fe62-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="6fe62-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





