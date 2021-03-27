---
title: Função D3DX_Saturate_FLOAT
description: Recupera o valor saturado do FLOAT fornecido.
ms.assetid: 659df450-3535-44eb-b867-89529369f903
keywords:
- Função D3DX_Saturate_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_Saturate_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3deabf5140d4f3f3bdfc2d6cce52f32385987ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837951"
---
# <a name="d3dx_saturate_float-function"></a><span data-ttu-id="98b29-104">\_Função float de saturação D3DX \_</span><span class="sxs-lookup"><span data-stu-id="98b29-104">D3DX\_Saturate\_FLOAT function</span></span>

<span data-ttu-id="98b29-105">Recupera o valor saturado do FLOAT fornecido.</span><span class="sxs-lookup"><span data-stu-id="98b29-105">Retrieves the saturated value of the given FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b29-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98b29-106">Syntax</span></span>

``` syntax
FLOAT D3DX_Saturate_FLOAT(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="98b29-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98b29-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98b29-108">*\_L*</span><span class="sxs-lookup"><span data-stu-id="98b29-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="98b29-109">O valor a ser saturado.</span><span class="sxs-lookup"><span data-stu-id="98b29-109">The value to saturate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98b29-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="98b29-110">Return value</span></span>

<span data-ttu-id="98b29-111">O valor saturado.</span><span class="sxs-lookup"><span data-stu-id="98b29-111">The saturated value.</span></span>

## <a name="requirements"></a><span data-ttu-id="98b29-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98b29-112">Requirements</span></span>



| <span data-ttu-id="98b29-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="98b29-113">Requirement</span></span> | <span data-ttu-id="98b29-114">Valor</span><span class="sxs-lookup"><span data-stu-id="98b29-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b29-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98b29-115">Header</span></span><br/> | <dl> <span data-ttu-id="98b29-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="98b29-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b29-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="98b29-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b29-118">Funções</span><span class="sxs-lookup"><span data-stu-id="98b29-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="98b29-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="98b29-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





