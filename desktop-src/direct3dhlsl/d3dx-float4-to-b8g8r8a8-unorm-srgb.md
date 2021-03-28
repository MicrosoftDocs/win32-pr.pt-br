---
title: Função D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
description: Compacta o XMFLOAT4 fornecido em um \_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB uint.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- Função D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c20292e1038d31c6d853eb8ae62f7e764e722a6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173128"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a><span data-ttu-id="191bb-104">D3DX \_ FLOAT4 \_ na \_ \_ função B8G8R8A8 UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="191bb-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="191bb-105">Compacta o XMFLOAT4 fornecido em um \_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB uint.</span><span class="sxs-lookup"><span data-stu-id="191bb-105">Packs the given XMFLOAT4 into a DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="191bb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="191bb-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="191bb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="191bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191bb-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="191bb-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="191bb-109">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="191bb-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="191bb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="191bb-110">Return value</span></span>

<span data-ttu-id="191bb-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="191bb-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="191bb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="191bb-112">Requirements</span></span>



| <span data-ttu-id="191bb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="191bb-113">Requirement</span></span> | <span data-ttu-id="191bb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="191bb-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="191bb-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="191bb-115">Header</span></span><br/> | <dl> <span data-ttu-id="191bb-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="191bb-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="191bb-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="191bb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="191bb-118">Funções</span><span class="sxs-lookup"><span data-stu-id="191bb-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="191bb-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="191bb-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





