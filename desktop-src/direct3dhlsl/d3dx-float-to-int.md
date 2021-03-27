---
title: Função D3DX_FLOAT_to_INT
description: Converte um valor FLOAT em INT.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- Função D3DX_FLOAT_to_INT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506531"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="e61e7-104">D3DX \_ flutuar \_ para \_ função int</span><span class="sxs-lookup"><span data-stu-id="e61e7-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="e61e7-105">Converte um valor FLOAT em INT.</span><span class="sxs-lookup"><span data-stu-id="e61e7-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61e7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e61e7-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="e61e7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e61e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61e7-108">*\_L*</span><span class="sxs-lookup"><span data-stu-id="e61e7-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="e61e7-109">O valor v.</span><span class="sxs-lookup"><span data-stu-id="e61e7-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="e61e7-110">*\_Escala*</span><span class="sxs-lookup"><span data-stu-id="e61e7-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="e61e7-111">O valor de escala.</span><span class="sxs-lookup"><span data-stu-id="e61e7-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e61e7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e61e7-112">Return value</span></span>

<span data-ttu-id="e61e7-113">O valor FLOAT convertido</span><span class="sxs-lookup"><span data-stu-id="e61e7-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="e61e7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61e7-114">Requirements</span></span>



| <span data-ttu-id="e61e7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61e7-115">Requirement</span></span> | <span data-ttu-id="e61e7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e61e7-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61e7-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e61e7-117">Header</span></span><br/> | <dl> <span data-ttu-id="e61e7-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e61e7-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61e7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e61e7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61e7-120">Funções</span><span class="sxs-lookup"><span data-stu-id="e61e7-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e61e7-121">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="e61e7-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





