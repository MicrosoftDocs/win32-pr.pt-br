---
title: Função D3DX_IsNan
description: Determina se o valor é um NaN (não um número).
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- Função D3DX_IsNan HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930726"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="355b8-104">\_Função D3DX IsNaN</span><span class="sxs-lookup"><span data-stu-id="355b8-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="355b8-105">Determina se o valor é um NaN (não um número).</span><span class="sxs-lookup"><span data-stu-id="355b8-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="355b8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="355b8-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="355b8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="355b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="355b8-108">*\_L*</span><span class="sxs-lookup"><span data-stu-id="355b8-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="355b8-109">O valor especificado.</span><span class="sxs-lookup"><span data-stu-id="355b8-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="355b8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="355b8-110">Return value</span></span>

<span data-ttu-id="355b8-111">verdadeiro se um NaN; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="355b8-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="355b8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="355b8-112">Requirements</span></span>



| <span data-ttu-id="355b8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="355b8-113">Requirement</span></span> | <span data-ttu-id="355b8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="355b8-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="355b8-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="355b8-115">Header</span></span><br/> | <dl> <span data-ttu-id="355b8-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="355b8-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="355b8-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="355b8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="355b8-118">Funções</span><span class="sxs-lookup"><span data-stu-id="355b8-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="355b8-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="355b8-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





