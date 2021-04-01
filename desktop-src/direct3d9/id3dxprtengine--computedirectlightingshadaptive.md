---
description: Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH), usando a amostragem adaptável.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'Método ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664114"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="29231-103">Método ID3DXPRTEngine:: ComputeDirectLightingSHAdaptive</span><span class="sxs-lookup"><span data-stu-id="29231-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="29231-104">Computa a contribuição de iluminação direta para objetos 3D onde o radiante de origem é representado por uma aproximação harmônica esférica (SH), usando a amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="29231-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="29231-105">Esse método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) de computação.</span><span class="sxs-lookup"><span data-stu-id="29231-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="29231-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29231-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="29231-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29231-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29231-108">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29231-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29231-109">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29231-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29231-110">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="29231-110">Order of the SH evaluation.</span></span> <span data-ttu-id="29231-111">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="29231-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="29231-112">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="29231-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="29231-113">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="29231-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="29231-114">*AdaptiveThresh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29231-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29231-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29231-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29231-116">Limite no vetor de PRT a ser usado para subdividir vértices de malha e rostos.</span><span class="sxs-lookup"><span data-stu-id="29231-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="29231-117">Se for menor que 1e-6F, um valor padrão de 1e-6F será especificado.</span><span class="sxs-lookup"><span data-stu-id="29231-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="29231-118">*MinEdgeLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29231-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29231-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29231-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29231-120">Comprimento mínimo de borda facial que será gerado na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="29231-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="29231-121">Se o método determinar que o valor é muito pequeno, um valor dependente de modelo será especificado.</span><span class="sxs-lookup"><span data-stu-id="29231-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="29231-122">Se for zero, um valor padrão de 4 será especificado.</span><span class="sxs-lookup"><span data-stu-id="29231-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="29231-123">*MaxSubdiv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29231-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29231-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29231-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29231-125">Nível máximo de subdivisão de uma face que será usada na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="29231-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="29231-126">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="29231-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29231-127">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="29231-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="29231-128">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="29231-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="29231-129">Esse buffer deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="29231-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29231-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29231-130">Return value</span></span>

<span data-ttu-id="29231-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="29231-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="29231-132">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29231-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="29231-133">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="29231-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="29231-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29231-134">Requirements</span></span>



| <span data-ttu-id="29231-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="29231-135">Requirement</span></span> | <span data-ttu-id="29231-136">Valor</span><span class="sxs-lookup"><span data-stu-id="29231-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29231-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29231-137">Header</span></span><br/>  | <dl> <span data-ttu-id="29231-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="29231-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="29231-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29231-139">Library</span></span><br/> | <dl> <span data-ttu-id="29231-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29231-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29231-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="29231-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29231-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="29231-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="29231-143">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="29231-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
