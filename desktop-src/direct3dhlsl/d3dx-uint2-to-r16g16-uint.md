---
title: Função D3DX_UINT2_to_R16G16_UINT
description: Compacta o XMUINT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ uint.
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- Função D3DX_UINT2_to_R16G16_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59a20b62fc5d8078152ed483ae49afceeeda4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989299"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a><span data-ttu-id="fbff5-104">D3DX \_ UINT2 \_ \_ R16G16 \_ função uint</span><span class="sxs-lookup"><span data-stu-id="fbff5-104">D3DX\_UINT2\_to\_R16G16\_UINT function</span></span>

<span data-ttu-id="fbff5-105">Compacta o XMUINT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="fbff5-105">Packs the given XMUINT2 back into a DXGI\_FORMAT\_R16G16\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbff5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbff5-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="fbff5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbff5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbff5-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="fbff5-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="fbff5-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="fbff5-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbff5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbff5-110">Return value</span></span>

<span data-ttu-id="fbff5-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="fbff5-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbff5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbff5-112">Requirements</span></span>



| <span data-ttu-id="fbff5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbff5-113">Requirement</span></span> | <span data-ttu-id="fbff5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fbff5-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbff5-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbff5-115">Header</span></span><br/> | <dl> <span data-ttu-id="fbff5-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fbff5-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbff5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbff5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbff5-118">Funções</span><span class="sxs-lookup"><span data-stu-id="fbff5-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fbff5-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="fbff5-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





