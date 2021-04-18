---
title: Função D3DX_SRGB_to_FLOAT_inexact
description: Converte um valor SRGB em FLOAT. | Função D3DX_SRGB_to_FLOAT_inexact
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- Função D3DX_SRGB_to_FLOAT_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968584"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="d1bee-105">D3DX \_ sRGB \_ para \_ flutuar \_ função inexata</span><span class="sxs-lookup"><span data-stu-id="d1bee-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="d1bee-106">Converte um valor SRGB em FLOAT.</span><span class="sxs-lookup"><span data-stu-id="d1bee-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1bee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1bee-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="d1bee-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1bee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1bee-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="d1bee-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="d1bee-110">Valor SRGB a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="d1bee-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1bee-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1bee-111">Return value</span></span>

<span data-ttu-id="d1bee-112">O valor de SRGB convertido.</span><span class="sxs-lookup"><span data-stu-id="d1bee-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1bee-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1bee-113">Remarks</span></span>

<span data-ttu-id="d1bee-114">Essa função não tem uma precisão alta o suficiente para fornecer a resposta exata.</span><span class="sxs-lookup"><span data-stu-id="d1bee-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="d1bee-115">A função alternativa [**D3DX \_ sRGB \_ para \_ flutuar**](d3dx-srgb-to-float.md) usa uma tabela de pesquisa para fornecer uma conversão exata de sRGB para float.</span><span class="sxs-lookup"><span data-stu-id="d1bee-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1bee-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1bee-116">Requirements</span></span>



| <span data-ttu-id="d1bee-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1bee-117">Requirement</span></span> | <span data-ttu-id="d1bee-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d1bee-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1bee-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1bee-119">Header</span></span><br/> | <dl> <span data-ttu-id="d1bee-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d1bee-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1bee-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1bee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1bee-122">Funções</span><span class="sxs-lookup"><span data-stu-id="d1bee-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="d1bee-123">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="d1bee-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





