---
title: Interface ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Uma interface de matriz-variável acessa uma matriz.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interface ID3DX11EffectMatrixVariable Direct3D 11
- Interface ID3DX11EffectMatrixVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968637"
---
# <a name="id3dx11effectmatrixvariable-interface"></a><span data-ttu-id="86656-105">Interface ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="86656-105">ID3DX11EffectMatrixVariable interface</span></span>

<span data-ttu-id="86656-106">Uma interface de matriz-variável acessa uma matriz.</span><span class="sxs-lookup"><span data-stu-id="86656-106">A matrix-variable interface accesses a matrix.</span></span>

## <a name="members"></a><span data-ttu-id="86656-107">Membros</span><span class="sxs-lookup"><span data-stu-id="86656-107">Members</span></span>

<span data-ttu-id="86656-108">A interface **ID3DX11EffectMatrixVariable** herda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="86656-108">The **ID3DX11EffectMatrixVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="86656-109">**ID3DX11EffectMatrixVariable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="86656-109">**ID3DX11EffectMatrixVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="86656-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="86656-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86656-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="86656-111">Methods</span></span>

<span data-ttu-id="86656-112">A interface **ID3DX11EffectMatrixVariable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="86656-112">The **ID3DX11EffectMatrixVariable** interface has these methods.</span></span>



| <span data-ttu-id="86656-113">Método</span><span class="sxs-lookup"><span data-stu-id="86656-113">Method</span></span>                                                                                 | <span data-ttu-id="86656-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="86656-114">Description</span></span>                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="86656-115">**Getmatrix**</span><span class="sxs-lookup"><span data-stu-id="86656-115">**GetMatrix**</span></span>](id3dx11effectmatrixvariable-getmatrix.md)                             | <span data-ttu-id="86656-116">Obter uma matriz.</span><span class="sxs-lookup"><span data-stu-id="86656-116">Get a matrix.</span></span><br/>                                          |
| [<span data-ttu-id="86656-117">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="86656-117">**GetMatrixArray**</span></span>](id3dx11effectmatrixvariable-getmatrixarray.md)                   | <span data-ttu-id="86656-118">Obtenha uma matriz de matrizes.</span><span class="sxs-lookup"><span data-stu-id="86656-118">Get an array of matrices.</span></span><br/>                              |
| [<span data-ttu-id="86656-119">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="86656-119">**GetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | <span data-ttu-id="86656-120">Transpor e obter uma matriz de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="86656-120">Transpose and get a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="86656-121">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="86656-121">**GetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | <span data-ttu-id="86656-122">Transpor e obter uma matriz de matrizes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="86656-122">Transpose and get an array of floating-point matrices.</span></span><br/> |
| [<span data-ttu-id="86656-123">**Setmatrix**</span><span class="sxs-lookup"><span data-stu-id="86656-123">**SetMatrix**</span></span>](id3dx11effectmatrixvariable-setmatrix.md)                             | <span data-ttu-id="86656-124">Defina uma matriz de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="86656-124">Set a floating-point matrix.</span></span><br/>                           |
| [<span data-ttu-id="86656-125">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="86656-125">**SetMatrixArray**</span></span>](id3dx11effectmatrixvariable-setmatrixarray.md)                   | <span data-ttu-id="86656-126">Defina uma matriz de matrizes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="86656-126">Set an array of floating-point matrices.</span></span><br/>               |
| [<span data-ttu-id="86656-127">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="86656-127">**SetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | <span data-ttu-id="86656-128">Transpor e definir uma matriz de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="86656-128">Transpose and set a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="86656-129">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="86656-129">**SetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | <span data-ttu-id="86656-130">Transpor e definir uma matriz de matrizes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="86656-130">Transpose and set an array of floating-point matrices.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86656-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="86656-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86656-132">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="86656-132">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="86656-133">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="86656-133">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="86656-134">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="86656-134">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86656-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86656-135">Requirements</span></span>



| <span data-ttu-id="86656-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="86656-136">Requirement</span></span> | <span data-ttu-id="86656-137">Valor</span><span class="sxs-lookup"><span data-stu-id="86656-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86656-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86656-138">Header</span></span><br/>  | <dl> <span data-ttu-id="86656-139"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="86656-139"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="86656-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86656-140">Library</span></span><br/> | <dl> <span data-ttu-id="86656-141"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="86656-141"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86656-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="86656-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86656-143">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="86656-143">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="86656-144">Efeitos 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="86656-144">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="86656-145">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="86656-145">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





