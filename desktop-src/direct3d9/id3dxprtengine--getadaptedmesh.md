---
description: Retorna uma malha com modificações resultantes da amostragem espacial adaptável. A malha retornada contém apenas posições, normais e coordenadas de textura (se definido).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'Método ID3DXPRTEngine:: GetAdaptedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298788"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="59952-104">Método ID3DXPRTEngine:: GetAdaptedMesh</span><span class="sxs-lookup"><span data-stu-id="59952-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="59952-105">Retorna uma malha com modificações resultantes da amostragem espacial adaptável.</span><span class="sxs-lookup"><span data-stu-id="59952-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="59952-106">A malha retornada contém apenas posições, normais e coordenadas de textura (se definido).</span><span class="sxs-lookup"><span data-stu-id="59952-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="59952-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59952-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="59952-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59952-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59952-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59952-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59952-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="59952-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="59952-111">Ponteiro para um dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que é usado para criar a malha de saída.</span><span class="sxs-lookup"><span data-stu-id="59952-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="59952-112">*pFaceRemap* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="59952-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59952-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59952-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59952-114">Ponteiro para a face de malha original que foi dividida para gerar a face atual.</span><span class="sxs-lookup"><span data-stu-id="59952-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="59952-115">*pVertRemap* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="59952-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59952-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59952-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59952-117">Ponteiro para uma matriz de destino que contém os três vértices de malha originais que são os pais do vértice atual.</span><span class="sxs-lookup"><span data-stu-id="59952-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="59952-118">*pfVertWeights* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="59952-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59952-119">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59952-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59952-120">Ponteiro para uma matriz de destino que contém fatores de mesclagem para os vértices pVertRemap.</span><span class="sxs-lookup"><span data-stu-id="59952-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="59952-121">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59952-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59952-122">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="59952-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="59952-123">Ponteiro para o objeto de malha [**ID3DXMesh**](id3dxmesh.md) de saída.</span><span class="sxs-lookup"><span data-stu-id="59952-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59952-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59952-124">Return value</span></span>

<span data-ttu-id="59952-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59952-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59952-126">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59952-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59952-127">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="59952-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="59952-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="59952-128">Remarks</span></span>

<span data-ttu-id="59952-129">pVertRemap e pfVertWeights podem ser usados para interpolar qualquer valor por vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="59952-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="59952-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59952-130">Requirements</span></span>



| <span data-ttu-id="59952-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="59952-131">Requirement</span></span> | <span data-ttu-id="59952-132">Valor</span><span class="sxs-lookup"><span data-stu-id="59952-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59952-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59952-133">Header</span></span><br/>  | <dl> <span data-ttu-id="59952-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59952-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59952-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59952-135">Library</span></span><br/> | <dl> <span data-ttu-id="59952-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59952-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59952-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="59952-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59952-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="59952-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
