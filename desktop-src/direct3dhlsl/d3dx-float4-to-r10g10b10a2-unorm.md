---
title: Função D3DX_FLOAT4_to_R10G10B10A2_UNORM
description: Compacta o XMFLOAT4 fornecido de volta em um \_ formato dxgi \_ R10G10B10A2 \_ UNORM.
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- Função D3DX_FLOAT4_to_R10G10B10A2_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c8d80b8822d03a43e813226c28dde8693397a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968544"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a><span data-ttu-id="422a5-104">D3DX \_ FLOAT4 \_ \_ R10G10B10A2 \_ UNORM function</span><span class="sxs-lookup"><span data-stu-id="422a5-104">D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM function</span></span>

<span data-ttu-id="422a5-105">Compacta o XMFLOAT4 fornecido de volta em um \_ formato dxgi \_ R10G10B10A2 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="422a5-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="422a5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="422a5-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="422a5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="422a5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="422a5-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="422a5-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="422a5-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="422a5-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="422a5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="422a5-110">Return value</span></span>

<span data-ttu-id="422a5-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="422a5-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="422a5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="422a5-112">Requirements</span></span>



| <span data-ttu-id="422a5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="422a5-113">Requirement</span></span> | <span data-ttu-id="422a5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="422a5-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="422a5-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="422a5-115">Header</span></span><br/> | <dl> <span data-ttu-id="422a5-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="422a5-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="422a5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="422a5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422a5-118">Funções</span><span class="sxs-lookup"><span data-stu-id="422a5-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="422a5-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="422a5-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





