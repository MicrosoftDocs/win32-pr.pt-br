---
title: all
description: Determina se todos os componentes do valor especificado são diferentes de zero.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- todos os HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967225"
---
# <a name="all"></a><span data-ttu-id="1947b-104">all</span><span class="sxs-lookup"><span data-stu-id="1947b-104">all</span></span>

<span data-ttu-id="1947b-105">Determina se todos os componentes do valor especificado são diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="1947b-105">Determines if all components of the specified value are non-zero.</span></span>



| <span data-ttu-id="1947b-106">*RET* todos (*x*)</span><span class="sxs-lookup"><span data-stu-id="1947b-106">*ret* all(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="1947b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1947b-107">Parameters</span></span>



| <span data-ttu-id="1947b-108">Item</span><span class="sxs-lookup"><span data-stu-id="1947b-108">Item</span></span>                                                   | <span data-ttu-id="1947b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1947b-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1947b-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="1947b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1947b-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="1947b-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1947b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1947b-112">Return Value</span></span>

<span data-ttu-id="1947b-113">**True** se todos os componentes do parâmetro *x* forem diferentes de zero; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1947b-113">**True** if all components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1947b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1947b-114">Remarks</span></span>

<span data-ttu-id="1947b-115">Essa função é semelhante à função intrínseca [**any**](dx-graphics-hlsl-any.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="1947b-115">This function is similar to the [**any**](dx-graphics-hlsl-any.md) HLSL intrinsic function.</span></span> <span data-ttu-id="1947b-116">A função **any** determina se qualquer componente do valor especificado é diferente de zero, enquanto a função **All** determina se todos os componentes do valor especificado são diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="1947b-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="1947b-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="1947b-117">Type Description</span></span>



| <span data-ttu-id="1947b-118">Name</span><span class="sxs-lookup"><span data-stu-id="1947b-118">Name</span></span>  | [<span data-ttu-id="1947b-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="1947b-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="1947b-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="1947b-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="1947b-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1947b-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="1947b-122">*x*</span><span class="sxs-lookup"><span data-stu-id="1947b-122">*x*</span></span>   | <span data-ttu-id="1947b-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="1947b-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="1947b-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1947b-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="1947b-125">any</span><span class="sxs-lookup"><span data-stu-id="1947b-125">any</span></span>  |
| <span data-ttu-id="1947b-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="1947b-126">*ret*</span></span> | [<span data-ttu-id="1947b-127">**escalar**</span><span class="sxs-lookup"><span data-stu-id="1947b-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="1947b-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="1947b-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="1947b-129">1</span><span class="sxs-lookup"><span data-stu-id="1947b-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1947b-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1947b-130">Minimum Shader Model</span></span>

<span data-ttu-id="1947b-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1947b-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1947b-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1947b-132">Shader Model</span></span>                                                                       | <span data-ttu-id="1947b-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1947b-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="1947b-134">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="1947b-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1947b-135">sim</span><span class="sxs-lookup"><span data-stu-id="1947b-135">yes</span></span>                   |
| [<span data-ttu-id="1947b-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1947b-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1947b-137">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="1947b-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1947b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1947b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1947b-139">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1947b-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

