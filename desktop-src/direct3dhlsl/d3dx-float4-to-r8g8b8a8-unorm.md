---
title: Função D3DX_FLOAT4_to_R8G8B8A8_UNORM
description: Desempacota \_ o formato dxgi \_ R8G8B8A8 \_ UNORM dados do sombreador para um XMFLOAT4. | Função D3DX_FLOAT4_to_R8G8B8A8_UNORM
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- Função D3DX_FLOAT4_to_R8G8B8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664097"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="269bd-105">D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM function</span><span class="sxs-lookup"><span data-stu-id="269bd-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="269bd-106">Desempacota \_ o formato dxgi \_ R8G8B8A8 \_ UNORM dados do sombreador para um XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="269bd-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="269bd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="269bd-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="269bd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="269bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="269bd-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="269bd-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="269bd-110">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="269bd-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="269bd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="269bd-111">Return value</span></span>

<span data-ttu-id="269bd-112">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="269bd-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="269bd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="269bd-113">Requirements</span></span>



| <span data-ttu-id="269bd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="269bd-114">Requirement</span></span> | <span data-ttu-id="269bd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="269bd-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="269bd-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="269bd-116">Header</span></span><br/> | <dl> <span data-ttu-id="269bd-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="269bd-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="269bd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="269bd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269bd-119">Funções</span><span class="sxs-lookup"><span data-stu-id="269bd-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="269bd-120">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="269bd-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





