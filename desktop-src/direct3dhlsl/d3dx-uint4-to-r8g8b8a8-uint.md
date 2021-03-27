---
title: Função D3DX_UINT4_to_R8G8B8A8_UINT
description: Compacta o XMUINT4 fornecido de volta em um \_ formato dxgi \_ R8G8B8A8 \_ uint.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- Função D3DX_UINT4_to_R8G8B8A8_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef8128d2d1989e986d8ff11e2d7e42e85f1fbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989297"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a><span data-ttu-id="02b43-104">D3DX \_ UINT4 \_ \_ R8G8B8A8 \_ função uint</span><span class="sxs-lookup"><span data-stu-id="02b43-104">D3DX\_UINT4\_to\_R8G8B8A8\_UINT function</span></span>

<span data-ttu-id="02b43-105">Compacta o XMUINT4 fornecido de volta em um \_ formato dxgi \_ R8G8B8A8 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="02b43-105">Packs the given XMUINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b43-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02b43-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="02b43-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02b43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02b43-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="02b43-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="02b43-109">Os dados do sombreador a serem empacotados.</span><span class="sxs-lookup"><span data-stu-id="02b43-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02b43-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02b43-110">Return value</span></span>

<span data-ttu-id="02b43-111">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="02b43-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="02b43-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02b43-112">Requirements</span></span>



| <span data-ttu-id="02b43-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="02b43-113">Requirement</span></span> | <span data-ttu-id="02b43-114">Valor</span><span class="sxs-lookup"><span data-stu-id="02b43-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02b43-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02b43-115">Header</span></span><br/> | <dl> <span data-ttu-id="02b43-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="02b43-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02b43-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="02b43-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b43-118">Funções</span><span class="sxs-lookup"><span data-stu-id="02b43-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="02b43-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="02b43-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





