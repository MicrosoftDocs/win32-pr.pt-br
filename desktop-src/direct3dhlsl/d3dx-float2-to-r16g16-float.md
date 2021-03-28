---
title: Função D3DX_FLOAT2_to_R16G16_FLOAT
description: Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ float.
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- Função D3DX_FLOAT2_to_R16G16_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849eb4dde5ab11e98675a1581519aabbeeb1e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989266"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a><span data-ttu-id="58771-104">D3DX \_ FLOAT2 \_ to \_ R16G16 \_ float function</span><span class="sxs-lookup"><span data-stu-id="58771-104">D3DX\_FLOAT2\_to\_R16G16\_FLOAT function</span></span>

<span data-ttu-id="58771-105">Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ float.</span><span class="sxs-lookup"><span data-stu-id="58771-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="58771-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58771-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="58771-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58771-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58771-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="58771-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="58771-109">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="58771-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58771-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58771-110">Return value</span></span>

<span data-ttu-id="58771-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="58771-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="58771-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58771-112">Requirements</span></span>



| <span data-ttu-id="58771-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="58771-113">Requirement</span></span> | <span data-ttu-id="58771-114">Valor</span><span class="sxs-lookup"><span data-stu-id="58771-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58771-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58771-115">Header</span></span><br/> | <dl> <span data-ttu-id="58771-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="58771-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58771-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="58771-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58771-118">Funções</span><span class="sxs-lookup"><span data-stu-id="58771-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="58771-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="58771-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





