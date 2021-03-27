---
title: Função D3DX_INT4_to_R8G8B8A8_SINT
description: Empacota o XMINT4 determinado de volta para um \_ formato dxgi \_ R8G8B8A8 \_ Santo.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- Função D3DX_INT4_to_R8G8B8A8_SINT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989278"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a><span data-ttu-id="63eab-104">D3DX \_ INT4 \_ para \_ R8G8B8A8 \_ Santo function</span><span class="sxs-lookup"><span data-stu-id="63eab-104">D3DX\_INT4\_to\_R8G8B8A8\_SINT function</span></span>

<span data-ttu-id="63eab-105">Empacota o XMINT4 determinado de volta para um \_ formato dxgi \_ R8G8B8A8 \_ Santo.</span><span class="sxs-lookup"><span data-stu-id="63eab-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="63eab-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63eab-106">Syntax</span></span>

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="63eab-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63eab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63eab-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="63eab-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="63eab-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="63eab-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63eab-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63eab-110">Return value</span></span>

<span data-ttu-id="63eab-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="63eab-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="63eab-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63eab-112">Requirements</span></span>



| <span data-ttu-id="63eab-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="63eab-113">Requirement</span></span> | <span data-ttu-id="63eab-114">Valor</span><span class="sxs-lookup"><span data-stu-id="63eab-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63eab-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63eab-115">Header</span></span><br/> | <dl> <span data-ttu-id="63eab-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="63eab-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63eab-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="63eab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63eab-118">Funções</span><span class="sxs-lookup"><span data-stu-id="63eab-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="63eab-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="63eab-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





