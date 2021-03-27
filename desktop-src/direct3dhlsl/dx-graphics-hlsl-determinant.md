---
title: determina
description: Retorna o determinante do ponto flutuante especificado, matriz quadrada.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- determinante HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967191"
---
# <a name="determinant"></a><span data-ttu-id="d2057-104">determina</span><span class="sxs-lookup"><span data-stu-id="d2057-104">determinant</span></span>

<span data-ttu-id="d2057-105">Retorna o determinante do ponto flutuante especificado, matriz quadrada.</span><span class="sxs-lookup"><span data-stu-id="d2057-105">Returns the determinant of the specified floating-point, square matrix.</span></span>



| <span data-ttu-id="d2057-106">determinante de *RET* (*m*)</span><span class="sxs-lookup"><span data-stu-id="d2057-106">*ret* determinant(*m*)</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="d2057-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2057-107">Parameters</span></span>



| <span data-ttu-id="d2057-108">Item</span><span class="sxs-lookup"><span data-stu-id="d2057-108">Item</span></span>                                                   | <span data-ttu-id="d2057-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2057-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="d2057-110"><span id="m"></span><span id="M"></span>*d*</span><span class="sxs-lookup"><span data-stu-id="d2057-110"><span id="m"></span><span id="M"></span>*m*</span></span><br/> | <span data-ttu-id="d2057-111">\[no \] valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d2057-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="d2057-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d2057-112">Return Value</span></span>

<span data-ttu-id="d2057-113">O valor escalar de ponto flutuante que representa o determinante do parâmetro *m* .</span><span class="sxs-lookup"><span data-stu-id="d2057-113">The floating-point, scalar value that represents the determinant of the *m* parameter.</span></span>

## <a name="type-description"></a><span data-ttu-id="d2057-114">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="d2057-114">Type Description</span></span>



| <span data-ttu-id="d2057-115">Name</span><span class="sxs-lookup"><span data-stu-id="d2057-115">Name</span></span>  | [<span data-ttu-id="d2057-116">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="d2057-116">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="d2057-117">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="d2057-117">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="d2057-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d2057-118">Size</span></span>                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="d2057-119">*m*</span><span class="sxs-lookup"><span data-stu-id="d2057-119">*m*</span></span>   | [<span data-ttu-id="d2057-120">**tabela**</span><span class="sxs-lookup"><span data-stu-id="d2057-120">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d2057-121">**barra**</span><span class="sxs-lookup"><span data-stu-id="d2057-121">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d2057-122">Any (número de linhas = número de colunas)</span><span class="sxs-lookup"><span data-stu-id="d2057-122">any (number of rows = number of columns)</span></span> |
| <span data-ttu-id="d2057-123">*RET*</span><span class="sxs-lookup"><span data-stu-id="d2057-123">*ret*</span></span> | [<span data-ttu-id="d2057-124">**escalar**</span><span class="sxs-lookup"><span data-stu-id="d2057-124">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="d2057-125">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="d2057-125">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="d2057-126">1</span><span class="sxs-lookup"><span data-stu-id="d2057-126">1</span></span>                                        |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d2057-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="d2057-127">Minimum Shader Model</span></span>

<span data-ttu-id="d2057-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d2057-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d2057-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="d2057-129">Shader Model</span></span>                                                                       | <span data-ttu-id="d2057-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="d2057-130">Supported</span></span>             |
|------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="d2057-131">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="d2057-131">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="d2057-132">sim</span><span class="sxs-lookup"><span data-stu-id="d2057-132">yes</span></span>                   |
| [<span data-ttu-id="d2057-133">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2057-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="d2057-134">vs \_ 1 \_ 1 e PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="d2057-134">vs\_1\_1 and ps\_1\_4</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="d2057-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2057-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2057-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="d2057-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

