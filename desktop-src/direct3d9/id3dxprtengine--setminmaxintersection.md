---
description: Define as distâncias mínimas e máximas de interseção entre objetos 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'Método ID3DXPRTEngine:: SetMinMaxIntersection (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298679"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="20d97-103">Método ID3DXPRTEngine:: SetMinMaxIntersection</span><span class="sxs-lookup"><span data-stu-id="20d97-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="20d97-104">Define as distâncias mínimas e máximas de interseção entre objetos 3D.</span><span class="sxs-lookup"><span data-stu-id="20d97-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="20d97-105">Esses valores de distância podem ser usados para controlar a distância mínima ou máxima que os objetos podem sombrear ou refletir a luz.</span><span class="sxs-lookup"><span data-stu-id="20d97-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="20d97-106">Por exemplo, o método pode ser usado para limitar a sombra dos recursos próximos de um modelo 3D.</span><span class="sxs-lookup"><span data-stu-id="20d97-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d97-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20d97-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="20d97-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20d97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20d97-109">*fMin* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20d97-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20d97-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20d97-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20d97-111">Distância mínima de interseção.</span><span class="sxs-lookup"><span data-stu-id="20d97-111">Minimum intersection distance.</span></span> <span data-ttu-id="20d97-112">Deve ser positivo e menor que fMax.</span><span class="sxs-lookup"><span data-stu-id="20d97-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="20d97-113">*fMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20d97-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20d97-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20d97-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20d97-115">Distância máxima de interseção.</span><span class="sxs-lookup"><span data-stu-id="20d97-115">Maximum intersection distance.</span></span> <span data-ttu-id="20d97-116">Se 0.0 f, o valor anterior será usado; caso contrário, deve ser maior que fMin.</span><span class="sxs-lookup"><span data-stu-id="20d97-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20d97-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20d97-117">Return value</span></span>

<span data-ttu-id="20d97-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20d97-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20d97-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20d97-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20d97-120">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="20d97-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="20d97-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="20d97-121">Remarks</span></span>

<span data-ttu-id="20d97-122">Esse método não pode ser usado em simulações de PRT (transferência de radiante de computação) executadas na GPU.</span><span class="sxs-lookup"><span data-stu-id="20d97-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="20d97-123">Consulte [**ID3DXPRTEngine:: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span><span class="sxs-lookup"><span data-stu-id="20d97-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20d97-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d97-124">Requirements</span></span>



| <span data-ttu-id="20d97-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d97-125">Requirement</span></span> | <span data-ttu-id="20d97-126">Valor</span><span class="sxs-lookup"><span data-stu-id="20d97-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20d97-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20d97-127">Header</span></span><br/>  | <dl> <span data-ttu-id="20d97-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="20d97-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="20d97-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20d97-129">Library</span></span><br/> | <dl> <span data-ttu-id="20d97-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20d97-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="20d97-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="20d97-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d97-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="20d97-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
