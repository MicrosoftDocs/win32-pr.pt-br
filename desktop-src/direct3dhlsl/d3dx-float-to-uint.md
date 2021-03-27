---
title: Função D3DX_FLOAT_to_UINT
description: Converte um valor FLOAT em UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- Função D3DX_FLOAT_to_UINT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298508"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="e2b6c-104">D3DX \_ flutuar \_ para \_ função uint</span><span class="sxs-lookup"><span data-stu-id="e2b6c-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="e2b6c-105">Converte um valor FLOAT em UINT.</span><span class="sxs-lookup"><span data-stu-id="e2b6c-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b6c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2b6c-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="e2b6c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2b6c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b6c-108">*\_L*</span><span class="sxs-lookup"><span data-stu-id="e2b6c-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="e2b6c-109">O vetor v.</span><span class="sxs-lookup"><span data-stu-id="e2b6c-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="e2b6c-110">*\_Escala*</span><span class="sxs-lookup"><span data-stu-id="e2b6c-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="e2b6c-111">O valor de escala.</span><span class="sxs-lookup"><span data-stu-id="e2b6c-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b6c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2b6c-112">Return value</span></span>

<span data-ttu-id="e2b6c-113">O valor FLOAT convertido</span><span class="sxs-lookup"><span data-stu-id="e2b6c-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b6c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2b6c-114">Requirements</span></span>



| <span data-ttu-id="e2b6c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b6c-115">Requirement</span></span> | <span data-ttu-id="e2b6c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e2b6c-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b6c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2b6c-117">Header</span></span><br/> | <dl> <span data-ttu-id="e2b6c-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e2b6c-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b6c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2b6c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b6c-120">Funções</span><span class="sxs-lookup"><span data-stu-id="e2b6c-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e2b6c-121">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="e2b6c-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





