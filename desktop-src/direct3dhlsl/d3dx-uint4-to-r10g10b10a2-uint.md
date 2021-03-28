---
title: Função D3DX_UINT4_to_R10G10B10A2_UINT
description: Compacta o XMINT4 fornecido de volta em um \_ formato dxgi \_ R10G10B10A2 \_ uint.
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- Função D3DX_UINT4_to_R10G10B10A2_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc7076b9e44ab1491bb8abbf8d4edb82158282c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989298"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a><span data-ttu-id="dc9d1-104">D3DX \_ UINT4 \_ \_ R10G10B10A2 \_ função uint</span><span class="sxs-lookup"><span data-stu-id="dc9d1-104">D3DX\_UINT4\_to\_R10G10B10A2\_UINT function</span></span>

<span data-ttu-id="dc9d1-105">Compacta o XMINT4 fornecido de volta em um \_ formato dxgi \_ R10G10B10A2 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9d1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc9d1-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="dc9d1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc9d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc9d1-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="dc9d1-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="dc9d1-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc9d1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc9d1-110">Return value</span></span>

<span data-ttu-id="dc9d1-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc9d1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc9d1-112">Requirements</span></span>



| <span data-ttu-id="dc9d1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc9d1-113">Requirement</span></span> | <span data-ttu-id="dc9d1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="dc9d1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9d1-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc9d1-115">Header</span></span><br/> | <dl> <span data-ttu-id="dc9d1-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="dc9d1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc9d1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc9d1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9d1-118">Funções</span><span class="sxs-lookup"><span data-stu-id="dc9d1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="dc9d1-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="dc9d1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





