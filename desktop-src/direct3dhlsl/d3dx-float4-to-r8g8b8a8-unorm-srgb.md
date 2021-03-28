---
title: Função D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
description: Compacta o XMFLOAT4 fornecido de volta em um \_ formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- Função D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f61e484675b94e1089436ce0b3bd564b3103a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298803"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a><span data-ttu-id="8893f-104">D3DX \_ FLOAT4 \_ na \_ \_ função R8G8B8A8 UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="8893f-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="8893f-105">Compacta o XMFLOAT4 fornecido de volta em um \_ formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="8893f-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="8893f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8893f-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8893f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8893f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8893f-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="8893f-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8893f-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="8893f-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8893f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8893f-110">Return value</span></span>

<span data-ttu-id="8893f-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="8893f-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8893f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8893f-112">Requirements</span></span>



| <span data-ttu-id="8893f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8893f-113">Requirement</span></span> | <span data-ttu-id="8893f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8893f-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8893f-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8893f-115">Header</span></span><br/> | <dl> <span data-ttu-id="8893f-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="8893f-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8893f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="8893f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8893f-118">Funções</span><span class="sxs-lookup"><span data-stu-id="8893f-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8893f-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="8893f-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





