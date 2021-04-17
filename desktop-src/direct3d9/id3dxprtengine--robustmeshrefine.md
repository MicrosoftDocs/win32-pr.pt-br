---
description: Subdivide faces em uma malha, permitindo uma amostragem adaptável conservadora que não eliminará os recursos na malha.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'Método ID3DXPRTEngine:: RobustMeshRefine (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782652"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="9c91b-103">Método ID3DXPRTEngine:: RobustMeshRefine</span><span class="sxs-lookup"><span data-stu-id="9c91b-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="9c91b-104">Subdivide faces em uma malha, permitindo uma amostragem adaptável conservadora que não eliminará os recursos na malha.</span><span class="sxs-lookup"><span data-stu-id="9c91b-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c91b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c91b-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="9c91b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c91b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c91b-107">*MinEdgeLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c91b-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c91b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c91b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c91b-109">Comprimento mínimo de borda facial que será gerado na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="9c91b-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="9c91b-110">Se for zero, um valor padrão razoável será substituído.</span><span class="sxs-lookup"><span data-stu-id="9c91b-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="9c91b-111">*MaxSubdiv* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c91b-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c91b-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c91b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c91b-113">Nível máximo de subdivisão de uma face que será usada na amostragem adaptável.</span><span class="sxs-lookup"><span data-stu-id="9c91b-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="9c91b-114">Se for zero, um valor padrão de 5 será substituído.</span><span class="sxs-lookup"><span data-stu-id="9c91b-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c91b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c91b-115">Return value</span></span>

<span data-ttu-id="9c91b-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c91b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c91b-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c91b-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9c91b-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9c91b-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c91b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c91b-119">Requirements</span></span>



| <span data-ttu-id="9c91b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c91b-120">Requirement</span></span> | <span data-ttu-id="9c91b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9c91b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c91b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c91b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9c91b-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c91b-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9c91b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c91b-124">Library</span></span><br/> | <dl> <span data-ttu-id="9c91b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c91b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c91b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c91b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c91b-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9c91b-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="9c91b-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span><span class="sxs-lookup"><span data-stu-id="9c91b-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="9c91b-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span><span class="sxs-lookup"><span data-stu-id="9c91b-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
