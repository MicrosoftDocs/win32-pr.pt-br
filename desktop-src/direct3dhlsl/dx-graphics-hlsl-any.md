---
title: any
description: Determina se qualquer componente do valor especificado é diferente de zero.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- qualquer HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967224"
---
# <a name="any"></a><span data-ttu-id="68cac-104">any</span><span class="sxs-lookup"><span data-stu-id="68cac-104">any</span></span>

<span data-ttu-id="68cac-105">Determina se qualquer componente do valor especificado é diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="68cac-105">Determines if any components of the specified value are non-zero.</span></span>



| <span data-ttu-id="68cac-106">*RET* qualquer (*x*)</span><span class="sxs-lookup"><span data-stu-id="68cac-106">*ret* any(*x*)</span></span> |
|----------------|



 

## <a name="parameters"></a><span data-ttu-id="68cac-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68cac-107">Parameters</span></span>



| <span data-ttu-id="68cac-108">Item</span><span class="sxs-lookup"><span data-stu-id="68cac-108">Item</span></span>                                                   | <span data-ttu-id="68cac-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="68cac-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="68cac-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="68cac-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="68cac-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="68cac-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="68cac-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="68cac-112">Return Value</span></span>

<span data-ttu-id="68cac-113">**True** se algum componente do parâmetro *x* for diferente de zero; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="68cac-113">**True** if any components of the *x* parameter are non-zero; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68cac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="68cac-114">Remarks</span></span>

<span data-ttu-id="68cac-115">Essa função é semelhante à função intrínseca [**All**](dx-graphics-hlsl-all.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="68cac-115">This function is similar to the [**all**](dx-graphics-hlsl-all.md) HLSL intrinsic function.</span></span> <span data-ttu-id="68cac-116">A função **any** determina se qualquer componente do valor especificado é diferente de zero, enquanto a função **All** determina se todos os componentes do valor especificado são diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="68cac-116">The **any** function determines if any components of the specified value are non-zero, while the **all** function determines if all components of the specified value are non-zero.</span></span>

## <a name="type-description"></a><span data-ttu-id="68cac-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="68cac-117">Type Description</span></span>



| <span data-ttu-id="68cac-118">Name</span><span class="sxs-lookup"><span data-stu-id="68cac-118">Name</span></span>  | [<span data-ttu-id="68cac-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="68cac-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="68cac-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="68cac-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="68cac-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="68cac-121">Size</span></span> |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="68cac-122">*x*</span><span class="sxs-lookup"><span data-stu-id="68cac-122">*x*</span></span>   | <span data-ttu-id="68cac-123">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="68cac-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | <span data-ttu-id="68cac-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="68cac-124">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="68cac-125">any</span><span class="sxs-lookup"><span data-stu-id="68cac-125">any</span></span>  |
| <span data-ttu-id="68cac-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="68cac-126">*ret*</span></span> | [<span data-ttu-id="68cac-127">**escalar**</span><span class="sxs-lookup"><span data-stu-id="68cac-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                            | [<span data-ttu-id="68cac-128">**bool**</span><span class="sxs-lookup"><span data-stu-id="68cac-128">**bool**</span></span>](/windows/desktop/WinProg/windows-data-types)                                                                                 | <span data-ttu-id="68cac-129">1</span><span class="sxs-lookup"><span data-stu-id="68cac-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="68cac-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="68cac-130">Minimum Shader Model</span></span>

<span data-ttu-id="68cac-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="68cac-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="68cac-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="68cac-132">Shader Model</span></span>                                                                       | <span data-ttu-id="68cac-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="68cac-133">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="68cac-134">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="68cac-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="68cac-135">sim</span><span class="sxs-lookup"><span data-stu-id="68cac-135">yes</span></span>                   |
| [<span data-ttu-id="68cac-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68cac-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="68cac-137">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="68cac-137">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="68cac-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="68cac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68cac-139">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="68cac-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

