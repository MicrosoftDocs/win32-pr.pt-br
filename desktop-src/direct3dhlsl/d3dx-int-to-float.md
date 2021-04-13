---
title: Função D3DX_INT_to_FLOAT
description: Converte um valor INT em FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- Função D3DX_INT_to_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968678"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="b3be8-104">D3DX \_ int \_ para a \_ função float</span><span class="sxs-lookup"><span data-stu-id="b3be8-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="b3be8-105">Converte um valor INT em FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b3be8-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3be8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3be8-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="b3be8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3be8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3be8-108">*\_L*</span><span class="sxs-lookup"><span data-stu-id="b3be8-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="b3be8-109">O valor v.</span><span class="sxs-lookup"><span data-stu-id="b3be8-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="b3be8-110">*\_Escala*</span><span class="sxs-lookup"><span data-stu-id="b3be8-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="b3be8-111">O valor de escala.</span><span class="sxs-lookup"><span data-stu-id="b3be8-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3be8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3be8-112">Return value</span></span>

<span data-ttu-id="b3be8-113">O valor int convertido.</span><span class="sxs-lookup"><span data-stu-id="b3be8-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3be8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3be8-114">Requirements</span></span>



| <span data-ttu-id="b3be8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3be8-115">Requirement</span></span> | <span data-ttu-id="b3be8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b3be8-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3be8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3be8-117">Header</span></span><br/> | <dl> <span data-ttu-id="b3be8-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="b3be8-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3be8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3be8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3be8-120">Funções</span><span class="sxs-lookup"><span data-stu-id="b3be8-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="b3be8-121">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="b3be8-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





