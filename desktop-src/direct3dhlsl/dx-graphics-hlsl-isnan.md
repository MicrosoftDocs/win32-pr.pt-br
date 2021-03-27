---
title: isNaN (Corecrt \_ Math. h)
description: Determina se o valor especificado é NAN ou QNAN.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- IsNaN HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9f4549b6a142f5bf6011cdfb144de92efde64c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012168"
---
# <a name="isnan"></a><span data-ttu-id="dcbfd-104">IsNaN</span><span class="sxs-lookup"><span data-stu-id="dcbfd-104">isnan</span></span>

<span data-ttu-id="dcbfd-105">Determina se o valor especificado é NAN ou QNAN.</span><span class="sxs-lookup"><span data-stu-id="dcbfd-105">Determines if the specified value is NAN or QNAN.</span></span>



| <span data-ttu-id="dcbfd-106">*RET* isNaN (*x*)</span><span class="sxs-lookup"><span data-stu-id="dcbfd-106">*ret* isnan(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="dcbfd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcbfd-107">Parameters</span></span>



| <span data-ttu-id="dcbfd-108">Item</span><span class="sxs-lookup"><span data-stu-id="dcbfd-108">Item</span></span>                                                   | <span data-ttu-id="dcbfd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcbfd-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="dcbfd-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="dcbfd-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="dcbfd-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="dcbfd-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="dcbfd-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dcbfd-112">Return Value</span></span>

<span data-ttu-id="dcbfd-113">Retorna um valor do mesmo tamanho que a entrada, com um valor definido como **true** se o parâmetro *x* for NaN ou QNAN.</span><span class="sxs-lookup"><span data-stu-id="dcbfd-113">Returns a value of the same size as the input, with a value set to **True** if the *x* parameter is NAN or QNAN.</span></span> <span data-ttu-id="dcbfd-114">Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="dcbfd-114">Otherwise, **False**.</span></span>

## <a name="type-description"></a><span data-ttu-id="dcbfd-115">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="dcbfd-115">Type Description</span></span>



| <span data-ttu-id="dcbfd-116">Name</span><span class="sxs-lookup"><span data-stu-id="dcbfd-116">Name</span></span>  | [<span data-ttu-id="dcbfd-117">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-117">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="dcbfd-118">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-118">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="dcbfd-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="dcbfd-119">Size</span></span>     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| <span data-ttu-id="dcbfd-120">*x*</span><span class="sxs-lookup"><span data-stu-id="dcbfd-120">*x*</span></span>   | <span data-ttu-id="dcbfd-121">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-121">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="dcbfd-122">**barra**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-122">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="dcbfd-123">any</span><span class="sxs-lookup"><span data-stu-id="dcbfd-123">any</span></span>      |
| <span data-ttu-id="dcbfd-124">*RET*</span><span class="sxs-lookup"><span data-stu-id="dcbfd-124">*ret*</span></span> | <span data-ttu-id="dcbfd-125">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-125">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="dcbfd-126">**bool**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-126">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                         | <span data-ttu-id="dcbfd-127">como entrada</span><span class="sxs-lookup"><span data-stu-id="dcbfd-127">as input</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dcbfd-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="dcbfd-128">Minimum Shader Model</span></span>

<span data-ttu-id="dcbfd-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dcbfd-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dcbfd-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="dcbfd-130">Shader Model</span></span>                                                                       | <span data-ttu-id="dcbfd-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="dcbfd-131">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="dcbfd-132">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="dcbfd-132">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="dcbfd-133">sim</span><span class="sxs-lookup"><span data-stu-id="dcbfd-133">yes</span></span>                 |
| [<span data-ttu-id="dcbfd-134">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dcbfd-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="dcbfd-135">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="dcbfd-135">yes (vs\_1\_1 only)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="dcbfd-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcbfd-136">Requirements</span></span>



| <span data-ttu-id="dcbfd-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcbfd-137">Requirement</span></span> | <span data-ttu-id="dcbfd-138">Valor</span><span class="sxs-lookup"><span data-stu-id="dcbfd-138">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbfd-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcbfd-139">Header</span></span><br/> | <dl> <span data-ttu-id="dcbfd-140"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcbfd-140"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcbfd-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcbfd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbfd-142">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="dcbfd-142">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

