---
title: comprimento
description: Retorna o comprimento do vetor de ponto flutuante especificado.
ms.assetid: eb06c87c-d536-448e-becb-762783cc2a77
keywords:
- comprimento HLSL
topic_type:
- apiref
api_name:
- length
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a7a93b0a7d225a25273a2ab4f8bf1d24656b6ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641238"
---
# <a name="length"></a><span data-ttu-id="ca4be-104">comprimento</span><span class="sxs-lookup"><span data-stu-id="ca4be-104">length</span></span>

<span data-ttu-id="ca4be-105">Retorna o comprimento do vetor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="ca4be-105">Returns the length of the specified floating-point vector.</span></span>



| <span data-ttu-id="ca4be-106">comprimento de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="ca4be-106">*ret* length(*x*)</span></span> |
|-------------------|



 

## <a name="parameters"></a><span data-ttu-id="ca4be-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca4be-107">Parameters</span></span>



| <span data-ttu-id="ca4be-108">Item</span><span class="sxs-lookup"><span data-stu-id="ca4be-108">Item</span></span>                                                   | <span data-ttu-id="ca4be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca4be-109">Description</span></span>                                     |
|--------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="ca4be-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="ca4be-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="ca4be-111">O vetor de ponto flutuante especificado.</span><span class="sxs-lookup"><span data-stu-id="ca4be-111">The specified floating-point vector.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ca4be-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ca4be-112">Return Value</span></span>

<span data-ttu-id="ca4be-113">Um escalar de ponto flutuante que representa o comprimento do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="ca4be-113">A floating-point scalar that represents the length of the *x* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="ca4be-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="ca4be-114">Type Description</span></span>



| <span data-ttu-id="ca4be-115">Name</span><span class="sxs-lookup"><span data-stu-id="ca4be-115">Name</span></span>  | [<span data-ttu-id="ca4be-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="ca4be-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="ca4be-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="ca4be-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="ca4be-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="ca4be-118">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="ca4be-119">*x*</span><span class="sxs-lookup"><span data-stu-id="ca4be-119">*x*</span></span>   | [<span data-ttu-id="ca4be-120">**vetor**</span><span class="sxs-lookup"><span data-stu-id="ca4be-120">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca4be-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="ca4be-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ca4be-122">any</span><span class="sxs-lookup"><span data-stu-id="ca4be-122">any</span></span>  |
| <span data-ttu-id="ca4be-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="ca4be-123">*ret*</span></span> | [<span data-ttu-id="ca4be-124">**escalar**</span><span class="sxs-lookup"><span data-stu-id="ca4be-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="ca4be-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="ca4be-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="ca4be-126">1</span><span class="sxs-lookup"><span data-stu-id="ca4be-126">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca4be-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ca4be-127">Minimum Shader Model</span></span>

<span data-ttu-id="ca4be-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca4be-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ca4be-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ca4be-129">Shader Model</span></span>                                                                       | <span data-ttu-id="ca4be-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ca4be-130">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="ca4be-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="ca4be-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="ca4be-132">sim</span><span class="sxs-lookup"><span data-stu-id="ca4be-132">yes</span></span>                 |
| [<span data-ttu-id="ca4be-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca4be-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="ca4be-134">Sim ( \_ apenas vs 1 \_ 1)</span><span class="sxs-lookup"><span data-stu-id="ca4be-134">yes (vs\_1\_1 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="ca4be-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca4be-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4be-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="ca4be-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

