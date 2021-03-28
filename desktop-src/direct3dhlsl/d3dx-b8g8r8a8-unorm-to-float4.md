---
title: Função D3DX_B8G8R8A8_UNORM_to_FLOAT4
description: Desempacota \_ o formato dxgi \_ B8G8R8A8 \_ UNORM dados do sombreador para um XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- Função D3DX_B8G8R8A8_UNORM_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bca17f350d40b1f74884232da9d1250bdb0abd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968553"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a><span data-ttu-id="aa0ed-104">D3DX \_ B8G8R8A8 \_ UNORM \_ \_ FLOAT4 function</span><span class="sxs-lookup"><span data-stu-id="aa0ed-104">D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="aa0ed-105">Desempacota \_ o formato dxgi \_ B8G8R8A8 \_ UNORM dados do sombreador para um XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="aa0ed-105">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa0ed-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="aa0ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa0ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa0ed-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="aa0ed-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="aa0ed-109">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="aa0ed-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa0ed-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa0ed-110">Return value</span></span>

<span data-ttu-id="aa0ed-111">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="aa0ed-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0ed-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa0ed-112">Requirements</span></span>



| <span data-ttu-id="aa0ed-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa0ed-113">Requirement</span></span> | <span data-ttu-id="aa0ed-114">Valor</span><span class="sxs-lookup"><span data-stu-id="aa0ed-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0ed-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa0ed-115">Header</span></span><br/> | <dl> <span data-ttu-id="aa0ed-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="aa0ed-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0ed-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa0ed-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0ed-118">Funções</span><span class="sxs-lookup"><span data-stu-id="aa0ed-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="aa0ed-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="aa0ed-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





