---
title: Função D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
description: Compacta o XMFLOAT3 fornecido de volta em um \_ formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- Função D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989289"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="bd57e-104">D3DX \_ FLOAT3 \_ na \_ \_ função B8G8R8X8 UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="bd57e-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="bd57e-105">Compacta o XMFLOAT3 fornecido de volta em um \_ formato dxgi \_ B8G8R8X8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="bd57e-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd57e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd57e-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="bd57e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd57e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd57e-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="bd57e-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="bd57e-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="bd57e-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd57e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd57e-110">Return value</span></span>

<span data-ttu-id="bd57e-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="bd57e-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd57e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd57e-112">Requirements</span></span>



| <span data-ttu-id="bd57e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd57e-113">Requirement</span></span> | <span data-ttu-id="bd57e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bd57e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd57e-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd57e-115">Header</span></span><br/> | <dl> <span data-ttu-id="bd57e-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="bd57e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd57e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd57e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd57e-118">Funções</span><span class="sxs-lookup"><span data-stu-id="bd57e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="bd57e-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="bd57e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





