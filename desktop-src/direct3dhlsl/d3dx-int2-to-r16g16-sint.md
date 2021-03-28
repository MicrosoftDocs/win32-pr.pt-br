---
title: Função D3DX_INT2_to_R16G16_SINT
description: Empacota o XMINT2 determinado de volta para um \_ formato dxgi \_ R16G16 \_ Santo.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- Função D3DX_INT2_to_R16G16_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968686"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="b62ed-104">D3DX \_ Int2 \_ para \_ R16G16 \_ Santo function</span><span class="sxs-lookup"><span data-stu-id="b62ed-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="b62ed-105">Empacota o XMINT2 determinado de volta para um \_ formato dxgi \_ R16G16 \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="b62ed-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="b62ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b62ed-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="b62ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b62ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b62ed-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="b62ed-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="b62ed-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="b62ed-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b62ed-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b62ed-110">Return value</span></span>

<span data-ttu-id="b62ed-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="b62ed-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b62ed-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b62ed-112">Requirements</span></span>



| <span data-ttu-id="b62ed-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b62ed-113">Requirement</span></span> | <span data-ttu-id="b62ed-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b62ed-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b62ed-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b62ed-115">Header</span></span><br/> | <dl> <span data-ttu-id="b62ed-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="b62ed-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b62ed-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b62ed-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b62ed-118">Funções</span><span class="sxs-lookup"><span data-stu-id="b62ed-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="b62ed-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="b62ed-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





