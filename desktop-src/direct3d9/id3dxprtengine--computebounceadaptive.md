---
description: Computa a radiante de origem resultante de um único salto de luz interrefletida, usando a amostragem adaptável.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'Método ID3DXPRTEngine:: ComputeBounceAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807836"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a><span data-ttu-id="e9131-103">Método ID3DXPRTEngine:: ComputeBounceAdaptive</span><span class="sxs-lookup"><span data-stu-id="e9131-103">ID3DXPRTEngine::ComputeBounceAdaptive method</span></span>

<span data-ttu-id="e9131-104">Computa a radiante de origem resultante de um único salto de luz interrefletida, usando a amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="e9131-104">Computes the source radiance resulting from a single bounce of interreflected light, using adaptive sampling.</span></span> <span data-ttu-id="e9131-105">Esse método gera novos vértices e rostos na malha para aproximar com mais precisão o sinal de radiante de transferência (PRT) de computação.</span><span class="sxs-lookup"><span data-stu-id="e9131-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span> <span data-ttu-id="e9131-106">Esse método pode ser usado para qualquer cena acesa, incluindo um modelo de PRT baseado em harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="e9131-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based PRT model.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9131-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9131-107">Syntax</span></span>


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="e9131-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9131-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9131-109">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9131-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9131-110">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e9131-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e9131-111">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa o objeto 3D do salto claro anterior.</span><span class="sxs-lookup"><span data-stu-id="e9131-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="e9131-112">Esse buffer de entrada deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="e9131-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e9131-113">*AdaptiveThresh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9131-113">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9131-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9131-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9131-115">Limite no vetor de PRT a ser usado para subdividir vértices de malha e rostos.</span><span class="sxs-lookup"><span data-stu-id="e9131-115">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="e9131-116">Se for menor que 1e-6F, um valor padrão de 1e-6F será especificado.</span><span class="sxs-lookup"><span data-stu-id="e9131-116">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e9131-117">*MinEdgeLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9131-117">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9131-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9131-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9131-119">Comprimento mínimo de borda facial que será gerado na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="e9131-119">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="e9131-120">Se o método determinar que o valor é muito pequeno, um valor dependente de modelo será especificado.</span><span class="sxs-lookup"><span data-stu-id="e9131-120">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="e9131-121">Se for zero, um valor padrão de 4 será especificado.</span><span class="sxs-lookup"><span data-stu-id="e9131-121">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="e9131-122">*MaxSubdiv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9131-122">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9131-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9131-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9131-124">Nível máximo de subdivisão de uma face que será usada na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="e9131-124">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="e9131-125">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e9131-125">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9131-126">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e9131-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e9131-127">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="e9131-127">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="e9131-128">Esse buffer de saída deve ter o número correto de canais de cores alocados para a simulação.</span><span class="sxs-lookup"><span data-stu-id="e9131-128">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="e9131-129">*pDataTotal* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e9131-129">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9131-130">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e9131-130">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e9131-131">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que mantém uma soma em execução de pDataOut com cada computação de retorno leve.</span><span class="sxs-lookup"><span data-stu-id="e9131-131">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that keeps a running sum of pDataOut with each light bounce computation.</span></span> <span data-ttu-id="e9131-132">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e9131-132">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9131-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9131-133">Return value</span></span>

<span data-ttu-id="e9131-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9131-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9131-135">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9131-135">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9131-136">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e9131-136">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9131-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9131-137">Requirements</span></span>



| <span data-ttu-id="e9131-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9131-138">Requirement</span></span> | <span data-ttu-id="e9131-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e9131-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9131-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9131-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e9131-141"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9131-141"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e9131-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9131-142">Library</span></span><br/> | <dl> <span data-ttu-id="e9131-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9131-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9131-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9131-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9131-145">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e9131-145">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e9131-146">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="e9131-146">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
