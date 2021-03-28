---
title: transpor
description: Transpõe a matriz de entrada especificada.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- transpor HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366124"
---
# <a name="transpose"></a><span data-ttu-id="04d5b-104">transpor</span><span class="sxs-lookup"><span data-stu-id="04d5b-104">transpose</span></span>

<span data-ttu-id="04d5b-105">Transpõe a matriz de entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="04d5b-105">Transposes the specified input matrix.</span></span>



| <span data-ttu-id="04d5b-106">Transpose de RET (*x*)</span><span class="sxs-lookup"><span data-stu-id="04d5b-106">ret transpose(*x*)</span></span> |
|--------------------|



 

## <a name="parameters"></a><span data-ttu-id="04d5b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04d5b-107">Parameters</span></span>



| <span data-ttu-id="04d5b-108">Item</span><span class="sxs-lookup"><span data-stu-id="04d5b-108">Item</span></span>                                                   | <span data-ttu-id="04d5b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="04d5b-109">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="04d5b-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="04d5b-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="04d5b-111">\[na \] matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="04d5b-111">\[in\] The specified matrix.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="04d5b-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="04d5b-112">Return Value</span></span>

<span data-ttu-id="04d5b-113">O valor transpodo do parâmetro *x* .</span><span class="sxs-lookup"><span data-stu-id="04d5b-113">The transposed value of the *x* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d5b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04d5b-114">Remarks</span></span>

<span data-ttu-id="04d5b-115">Se as dimensões da matriz de origem forem  *colunas* de linhas, a matriz resultante será as *linhas* de *colunas* .</span><span class="sxs-lookup"><span data-stu-id="04d5b-115">If the dimensions of the source matrix are *rows* *columns*, the resulting matrix is *columns* *rows*.</span></span>

## <a name="type-description"></a><span data-ttu-id="04d5b-116">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="04d5b-116">Type Description</span></span>



| <span data-ttu-id="04d5b-117">Name</span><span class="sxs-lookup"><span data-stu-id="04d5b-117">Name</span></span> | [<span data-ttu-id="04d5b-118">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="04d5b-118">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="04d5b-119">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="04d5b-119">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                         | <span data-ttu-id="04d5b-120">Tamanho</span><span class="sxs-lookup"><span data-stu-id="04d5b-120">Size</span></span>                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04d5b-121">*x*</span><span class="sxs-lookup"><span data-stu-id="04d5b-121">*x*</span></span>  | [<span data-ttu-id="04d5b-122">**tabela**</span><span class="sxs-lookup"><span data-stu-id="04d5b-122">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="04d5b-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="04d5b-123">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="04d5b-124">any</span><span class="sxs-lookup"><span data-stu-id="04d5b-124">any</span></span>                                                                                    |
| <span data-ttu-id="04d5b-125">RET</span><span class="sxs-lookup"><span data-stu-id="04d5b-125">ret</span></span>  | [<span data-ttu-id="04d5b-126">**tabela**</span><span class="sxs-lookup"><span data-stu-id="04d5b-126">**matrix**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="04d5b-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="04d5b-127">[**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types)</span></span> | <span data-ttu-id="04d5b-128">linhas = mesmo número de colunas como *x* de entrada, colunas = mesmo número de linhas como *x* de entrada</span><span class="sxs-lookup"><span data-stu-id="04d5b-128">rows = same number of columns as input *x*, columns = same number of rows as input *x*</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="04d5b-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="04d5b-129">Minimum Shader Model</span></span>

<span data-ttu-id="04d5b-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="04d5b-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="04d5b-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="04d5b-131">Shader Model</span></span>                                                                       | <span data-ttu-id="04d5b-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="04d5b-132">Supported</span></span> |
|------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="04d5b-133">[Modelo do sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="04d5b-133">[Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) and higher shader models</span></span> | <span data-ttu-id="04d5b-134">sim</span><span class="sxs-lookup"><span data-stu-id="04d5b-134">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="04d5b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="04d5b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d5b-136">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="04d5b-136">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

